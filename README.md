## QuadraticConverter

### Extension for RoboFont

**QuadraticConverter** is an extension for RoboFont that converts Cubic (PostScript) UFO to Quadratic (TrueType) UFO.

It might be installed manually ([download](https://github.com/sansplomb/QuadraticConverter/archive/master.zip) and double-click) or automatically with [*RoboFont Mechanic*](http://www.robofontmechanic.com).

Copyright (c) 2015, Samuel Hornus and Jérémie Hornus

## Changes

- **0.7.1**
  - Fixed crash when the font has less than 20 glyphs
- **0.7**
  - Improved the low-level approximation technique. This results in **much** fewer generated control points
- **0.6.2**
  - Improved sensitivity of the closeness of a quadratic and a cubic curve. This lowers the number of control points required for given precision
- **0.6.1**
  - Added a button to convert a single glyph from an existing cubic layer. This is useful for fine-tuning a converted font (use the "*Cubic contour*" layer)
- **0.6**
  - Faster by not using the slow `contour.autoStartSegment()`
  - Optimized code
  - Slightly better approximation in non-smooth segments
- **0.5.9**
  - The conversion avoids inserting some inflection points
  - The approximation of a cubic by a single quadratic is more robust
- **0.5.8**
  - Fixed wrong approximation when a handle has length zero
- **0.5.7**
  - Improved behavior when glyph has both contours and components
- **0.5.6**
  - Added option to subdivide the smooth segments by arc-length (enabled by default)
- **0.5.5**
  - The contours are correctly orderer for the hinting to perform correctly
- **0.5.4**
  - Converting a UFO will create a new UFO. Converting a non-UFO modifies it in place
  - In any case, the original contour is saved in the layer *Cubic contour*
  - New control for the minimum length of a quadratic segment
