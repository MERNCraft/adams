# Enlightenment? #

[Demo](https://MERNCraft.github.io/adams)

A CSS-only demo of using `:hover`, `counter`s and `@counter-styles` to create interaction.

The stairs are nested `<div>`s, so hovering the mouse (or tapping on a touchscreen) will make the browser create a `:hover` pseudo-class for the element under the pointer and all of its parents.

A `@counter-style` is defined with each item a word in a quote from Douglas Adams. The `:hover` rule for each step generates an `::after` pseudo-element which creates its own `counter` and uses that to display a word from the quote.

> This is is fact overkill. It would be simpler to get each `::after` element to display its own hard-coded word. This technique, however could be used to increment a counter for each `:hover` pseudo-class that is created, and possibly to perform further calculations before displaying a `counter` value.

To prevent you from moving directly to the top of the stairs, each step has a rule that hides a mask that covers the step above. Only by moving up the stairs one at a time can you create a `:hover` pseudo-class for each step.

The steps are created from a number of `<div>` elements. It would have been possible to use `::before` and `::after` pseudo-elements to create the rotated shapes that produce a realistic outline for each step, but here `<div>` elements were used for these shapes too.