# What are some differences between interfaces and types in TypeScript?

| Type                                                                  | Interface                                                              | Notes                                                                                     |
| :-------------------------------------------------------------------- | :--------------------------------------------------------------------- | :---------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| Types can be used as alias for both primitive and non primitive types | Interface can be used only for objects and classes                     |                                                                                           |
| Union types can only be used with types eg. `type name = string       | number`                                                                | There is no direct union type for interfaces, but we can create a union of two interfaces | This row was split across two columns in your original. Corrected. |
| Use intersection (`&`) to inherit from other types                    | Use `extends` to inherit from other interfaces                         |                                                                                           |
| Using intersection is less performant                                 | Using extending is more performant than intersection and more readable |                                                                                           |

# What is the use of the keyof keyword in TypeScript? Provide an example.

`keyof` keyword is used to create union type of keys of object type.
Example:

<pre> ```ts
interface person {
name: string;
age: number
}

type newType = keyof person
</pre>

Now newType would be name | age

We can also use `keyof`to constrain parameters of a function
