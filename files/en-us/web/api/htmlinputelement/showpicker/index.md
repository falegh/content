---
title: HTMLInputElement.showPicker()
slug: Web/API/HTMLInputElement/showPicker
tags:
  - API
  - HTML DOM
  - HTMLInputElement
  - Method
  - NeedsCompatTable
  - Reference
browser-compat: api.HTMLInputElement.showPicker
---
{{ APIRef("HTML DOM") }}

The **`HTMLInputElement.showPicker()`** method shows a browser picker to the
user.

A browser picker is shown when the element is one of these types: `"date"`,
`"month"`, `"week"`, `"time"`, `"datetime-local"`, `"color"`, or `"file"`. It
can also be prepopulated with items from a {{htmlelement("datalist")}} element or [`autocomplete`](/en-US/docs/Web/HTML/Attributes/autocomplete) attribute.

### Return value

{{jsxref("undefined")}}.

### Exceptions

- `NotAllowedError` {{domxref("DOMException")}}
  - : Thrown if not called in response to a user gesture such as a touch gesture
    or mouse click.
- `SecurityError` {{domxref("DOMException")}}
  - : Thrown if called in a cross-origin iframe.

## Syntax

```js
showPicker()
```

### Parameters

None.

## Examples

Click the button in this example to show a color picker.

### HTML

```html
<input type="color">
<button>Show the color picker</button>
```

### JavaScript

```js
const button = document.querySelector("button");
const colorInput = document.querySelector("input");

button.addEventListener("click", () => {
  try {
    colorInput.showPicker();
    // A color picker is shown.
  } catch (error) {
    window.alert(error);
    // Use external library when this fails.
  }
});
```

### Result

{{EmbedLiveSample("Examples")}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{ HTMLElement("input") }}
- {{ domxref("HTMLInputElement") }}
