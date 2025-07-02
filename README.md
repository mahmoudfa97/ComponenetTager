# component-tagger

A powerful JSX transformer plugin for **React** that injects a full set of metadata attributes into every React component during the build process. This enables advanced **debugging**, **analytics**, **visual editing**, **live previews**, or **no-code UI overlays**.

---

### What It Does

Transforms:

```tsx
<MyComponent />
```
into: 
```tsx
<MyComponent
  data-mwf-id="abc123"
  data-mwf-name="MyComponent"
  data-mwf-path="components/MyComponent.tsx"
  data-mwf-line="12"
  data-mwf-file="MyComponent.tsx"
  data-mwf-component="MyComponent"
  data-mwf-content="%7B%22type%22%3A...%7D"
/>
```
 Injected Attributes:

| Attribute            | Description                              |
| -------------------- | ---------------------------------------- |
| `data-mwf-id`        | Unique hash per element instance         |
| `data-mwf-name`      | React component name                     |
| `data-mwf-path`      | Relative path of the file                |
| `data-mwf-line`      | Line number in source                    |
| `data-mwf-file`      | Source file name                         |
| `data-mwf-component` | Redundant name for easier querying       |
| `data-mwf-content`   | URI-encoded JSON of original JSX element |

Use Cases:
- A/B testing (e.g. uniquely identify every component variant)

- DOM-based analytics (Google Tag Manager, heatmaps)

- Live preview editors / in-app CMS overlays

- Developer tools (like auto-scroll to component in source)

- In-browser component traceability (inspect-to-source)

How to use:
- clone and import it in your SWC config
- ![image](https://github.com/user-attachments/assets/606e7023-a86c-4805-a3ba-a4c4444034ed)


 Tech Stack"
- Written in TypeScript

- Uses SWC plugin hooks

- Fully static: zero runtime overhead
  
Preview:
![image](https://github.com/user-attachments/assets/1553ac40-a002-4475-9aed-9ca67792745d)


Contributing:
- Got ideas or use cases? PRs and issues welcome!


