# TLDR Rust


## 3.3 Variables and Mutability 

Rust has type inference. Default integer is i32. Default float is f64. 

The compiler can look at the left side of an assignment to inform the inference engine.

To create a variable, use the `let` keyword. This creates an immutable (readonly) variable. The compiler will ensure it will not change after it is declared and assigned. 

`let mut` creates a mutable (readwrite) variable. This creates a variable identical to those found in imperative languages like Python, C, or C++.

### Constants

Constants start with the keyword `const`.

Constants are similar to readonly variables with the following differences: 

 * can only be set at compile time 
 * can only be set with a constant expression 

Constants in Rust are legal to put in any scope and are valid for the entire scope. 

See the reference section on `constants` for more info https://doc.rust-lang.org/reference/const_eval.html

### Shadowing

A useful feature that comes from functional programming is `shadowing`. This feature most likely comes from `ocaml`. 

`Shadowing` means that an immutable (readonly) variable can be hidden by the creation of another immutable variable (readonly) with the same name. 

For example, in Rust you can declare the same variable multiple times in the same scope. 

    let x = 10; 
    let x = 11;

While this appears to be reassigning the same variable, what is happening is the original `x` is being hidden and a new variable is being created with the value 11.

One consequence of this is that the datatype of `x` can also change in the process since a new variable is being created. 




