# Key points of 'Why Should Engineers and Scientists Be Worried About Color?'

IBM did research in the 90s on perceptually-based color maps and how to best represent various types of data within the color dimensions of luminescence, saturation and hue.
These perceptually-based color maps can help represent features in the data and prevent visual artifacts, which could be erroneously interpreted as structures in the data.

## Problem

Standard uses of color can distort the meaning of the underlying data, and can lead to incorrect evaluations, conclusions or decisions.

## Solution

Create a set of color maps which take into account the
- data type, 
- spatial frequency of the data
- properties of the human perceptual system.

## Results

- Hue was not a good dimension for encoding magnitude information, i.e. Rainbow color maps are bad.

### Data types
- For interval data, use isomorphic color maps, i.e. equal steps in the data corresponds to equal perceptual steps in the colormap.
- For ratio data, use same color map and in addition, represent the zero of the scale.
- Threshold values in the scale have a significant meaning. Capture the transition explicitly via a perceived discontinuity.

### Spatial frequency of data
For interval and ratio data, both luminance- and saturation-varying color map should produce the effect of having equal steps in data value correspond to equal perceptual steps. But
- Luminance variations across the data range are better at conveying variations in the magnitude of high spatial frequency (noisy) data.
- Saturation variations are better at conveying variations in the magnitude of low spatial frequency (smoothly varying) data.  

### Visual representations
Different representations are required depending on whether the goal of visualization is exploration or presentation:
- Use an isomorphic color map, when you want to produce a faithful color map of the structure in the data,
- Use a segmented color map,   when you want to show how particular ranges of a variable are distributed over the image,
- Use a highlight color map,   When you want to draw the user's attention to regions in the image which have certain characteristics,

Using all three perceptually-based representations in concert allows the analyst to gain a more sophisticated insight into the data.
