# A Simple GUI Library

Let us design a classical GUI library using our new knowledge of traits and trait objects.

We will have a number of widgets in our library:

- Window: has a title and contains other widgets.
- Button: has a label and a callback function which is invoked when the button is pressed.
- Label: has a label.

The widgets will implement a Widget trait.

The output of the above program can be something simple like this:

```bash
========
Rust GUI Demo 1.23
========

This is a small text GUI demo.

| Click me! |

```

If you want to draw aligned text, you can use the *fill/alignment* formatting operators. In particular, notice how you can pad with different characters (here a '/') and how you can control alignment:

```rust
fn main() {
    let width = 10;
    println!("left aligned:  |{:/<width$}|", "foo");
    println!("centered:      |{:/^width$}|", "foo");
    println!("right aligned: |{:/>width$}|", "foo");
}
```

Using such alignment tricks, you can for example produce output like this:

```bash
+--------------------------------+
|       Rust GUI Demo 1.23       |
+================================+
| This is a small text GUI demo. |
| +-----------+                  |
| | Click me! |                  |
| +-----------+                  |
+--------------------------------+

```