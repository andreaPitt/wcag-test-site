# WCAG Testing Site
This site is for testing automated detection of failures of WCAG criteria using various testing software.

The failures included are:

## Test Images

### 1.1.1 - All non-text content that is presented to the user has a text alternative that serves the equivalent purpose (except for some specific situations like decorative content).

### Images using \<img\> tag
1. With alt attribute
    - Expected outcome: Pass 
2. Without alt attribute
    - Expected outcome: Fail automated tool and AI tool
3. With inaccurate alt attribute
    - Expected outcome: Pass automated tool, fail AI tool
4. With empty alt attribute
    - Expected outcome: Pass automated tool, fail AI tool

### Active Images
1. Linked logo with alt attribute
    - Expected outcome: Pass
2. Linked logo with empty alt attribute
    - Expected outcome: Fail automated tool and AI tool
3. Linked logo without alt attribute
    - Expected outcome: Fail automated tool and AI tool
4. Linked logo with inaccurate alt attribute
    - Expected outcome: Pass automated tool, fail AI Tool

### Input Images
1. Input image with alt attribute
    - Expected outcome: Pass
2. Input image with inaccurate alt attribute
    - Expected outcome: Pass automated tool, fail AI tool.
3. Input image with empty alt attribute
    - Expected outcome: Fail automated tool and AI tool

### SVG Images
1. SVG with title
    - Expected outcome: Pass
3. SVG without title
    - Expected outcome: Fail automated tool and AI tool
4. SVG with inaccurate title
    - Expected outcome: Pass automated tool, fail AI tool

### Canvas
1. Canvas element with aria-label
    - Expected outcome: Pass
2. Canvas element without aria-label
    - Expected outcome: Pass automated tool, fail AI tool

### Object tag
1. Object element with title attribute
    - Expected outcome: Pass
2. Object element without title attribute
    - Expected outcome: Fail automated tool and AI tool
3. Object element with inaccurate title attribute
    - Expected outcome: Pass automated tool, fail AI tool

### Complex image
1. Image with alt text, but no long description. Such as 
```
<p id="longdesc">
    This diagram illustrates the water cycle, including processes such as evaporation, condensation, precipitation, and collection. Water evaporates from oceans and lakes, rises into the atmosphere, condenses into clouds, and eventually falls back to the earth as precipitation, collecting in bodies of water to start the cycle again.
</p>
```
- Expected outcome: Pass automated tool, fail AI tool

### Background Images
1. Background image with role="img" and aria-label attribute
    - Expected outcome: Pass
2. Background image without role="img" and aria-label attribute
    - Expected outcome: Pass automated tool, fail AI tool