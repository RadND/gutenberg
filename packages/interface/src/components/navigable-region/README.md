# NavigableRegion

`NavigableRegion` renders an ARIA landmark region that's meant to be used together with the `useNavigateRegions` component from the `@wordpress/components` package. The ARIA landmark is a `div` element with a `role="region"` attribute and an `aria-label` attribute. It's made focusable by the means of a `tabindex="-1"` attribute so that `useNavigateRegions` can set focus on it and allow keyboard navigation through the regions in the editor.

It also renders a child `div` element that is responsible to set a negative `z-index` stack level, to make sure the focus style is always visible, regardless of other elements that may cut-off the focus style outline otherwise.

It can use a CSS animation via the `motion` component.

## Props

### children

The component that should be rendered as content.

-   Type: React Element
-   Required: Yes

### className

The CSS class that will be added to the classes of the wrapper div.

-   Type: `String`
-   Required: No

### ariaLabel

A meaningful name for the ARIA landmark region.

-   Type: `String`
-   Required: Yes

### motionProps

Properties of `motionProps` object will be used by the `motion` component to set a CSS animation on the wrapper div.

-   Type: `Object`
-   Required: No
-   Default: `{}`
