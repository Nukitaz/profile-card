# Checkpoint Questions

1. **What is the default value of `flexDirection` in React Native? How is it different from CSS on the web?**
   In React Native, the default value of `flexDirection` is `'column'`, meaning child elements stack vertically from top to bottom. On the web, CSS Flexbox defaults to `'row'`, which arranges elements horizontally from left to right.

2. **What is the difference between `justifyContent` and `alignItems`?**
   `justifyContent` aligns child elements along the primary axis (vertical when `flexDirection` is `'column'`, horizontal when `'row'`). `alignItems` aligns child elements along the cross axis, which is perpendicular to the primary axis.

3. **What does `flex: 1` do inside a row? And on the outermost `View` of a screen?**
   Inside a row, `flex: 1` makes the component expand horizontally to fill all remaining available space (or share space equally among siblings that also have `flex: 1`). On the outermost `View` of a screen, `flex: 1` instructs the container to expand and occupy 100% of the device's viewport height.

4. **What is the difference between `resizeMode="cover"` and `resizeMode="contain"`?**
   `resizeMode="cover"` scales the image uniformly so that it completely fills the container's bounds, cropping any parts that overflow while preserving the aspect ratio. `resizeMode="contain"` scales the entire image to fit inside the container without cropping, which may leave empty space if the aspect ratios do not match.

5. **Why do we use `StyleSheet.create` instead of plain objects inside the JSX?**
   `StyleSheet.create` validates style properties at compile/bundle time and registers the styles once instead of recreating new style objects on every render. This prevents unnecessary memory allocations and improves rendering performance.

6. **Why does a shadow written with `shadowColor` not appear on Android?**
   Properties like `shadowColor`, `shadowOffset`, `shadowOpacity`, and `shadowRadius` are iOS-specific and map directly to Core Animation layers. Android uses Material Design's native `elevation` property to render drop shadows instead.