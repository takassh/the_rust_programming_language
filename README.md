# What is this repository?
To learn Rust based on [document](https://doc.rust-lang.org/book/title-page.html)

# Common Questions
Because the document is really helpful to understand programming, not only Rust itself, I summarize common questions which I make as if I were the biginner of programming, and answer the questions shortly. I added two types: R or G, which distinguish whether the question topic is about Rust itself or general programming after each question.

## Why do we use Enum? [G]
- Enums give you a way of saying a value is one of a possible set of values. For example, let's say we deal with IP addresses: ipv4 and ipv6. IP adress can take one of them, but **not both at the same time**. In this case, we would rather use Enum than structs.

## Why doesn't Rust have null? [R]
- Because null brings errors to our code easily. In some other languages, variables can always be null or not-null. However, when we assume a variable isn't null but it actually is, null error happens although null concept itself is useful. In Rust, instead of Null, you can use `Option<T>` which is one of Enums. Before you use `Option<T>`, you have to check if the variable is really present or absent. This can take advantage of null concept and at the same time it's safe to be used.
- ref: "Null References: The Billion Dollar Mistake,” Tony Hoare.

## Why do we want to use absolute path to call other module? [R]
- Because it's more likely we'll want to move our code definitions and item calls independently of each other

## Why do we specify the parent of a function and specify the full path of a struct? [R]
- When we use function, we care about the place in which it's built, and this is idiomatic. When we use struct, there is no strong reason to use the full path.