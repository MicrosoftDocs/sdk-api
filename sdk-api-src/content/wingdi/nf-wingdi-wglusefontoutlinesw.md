---
UID: NF:wingdi.wglUseFontOutlinesW
title: wglUseFontOutlinesW function (wingdi.h)
description: The wglUseFontOutlines function creates a set of display lists, one for each glyph of the currently selected outline font of a device context, for use with the current rendering context. (Unicode)
helpviewer_keywords: ["_ogl_wglUseFontOutlines", "opengl.wglusefontoutlines", "wglUseFontOutlines", "wglUseFontOutlines function [OpenGL]", "wglUseFontOutlinesW", "wingdi/wglUseFontOutlines", "wingdi/wglUseFontOutlinesW"]
old-location: opengl\wglusefontoutlines.htm
tech.root: OpenGL
ms.assetid: 08a86563-c6ca-4efb-9096-bc487fc5037c
ms.date: 12/05/2018
ms.keywords: _ogl_wglUseFontOutlines, opengl.wglusefontoutlines, wglUseFontOutlines, wglUseFontOutlines function [OpenGL], wglUseFontOutlinesA, wglUseFontOutlinesW, wingdi/wglUseFontOutlines, wingdi/wglUseFontOutlinesA, wingdi/wglUseFontOutlinesW
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: wglUseFontOutlinesW (Unicode) and wglUseFontOutlinesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - wglUseFontOutlinesW
 - wingdi/wglUseFontOutlinesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglUseFontOutlines
 - wglUseFontOutlinesA
 - wglUseFontOutlinesW
---

# wglUseFontOutlinesW function


## -description

The <b>wglUseFontOutlines</b> function creates a set of display lists, one for each glyph of the currently selected outline font of a device context, for use with the current rendering context. The display lists are used to draw 3-D characters of TrueType fonts. Each display list describes a glyph outline in floating-point coordinates.

The run of glyphs begins with thefirstglyph of the font of the specified device context. The em square size of the font, the notional grid size of the original font outline from which the font is fitted, is mapped to 1.0 in the x- and y-coordinates in the display lists. The extrusion parameter sets how much depth the font has in the z direction.

Thelpgmfparameter returns a <a href="/windows/desktop/api/wingdi/ns-wingdi-glyphmetricsfloat">GLYPHMETRICSFLOAT</a> structure that contains information about the placement and orientation of each glyph in a character cell.

## -parameters

### -param unnamedParam1

Specifies the device context with the desired outline font. The outline font of <i>hdc</i> is used to create the display lists in the current rendering context.

### -param unnamedParam2

Specifies the first of the set of glyphs that form the font outline display lists.

### -param unnamedParam3

Specifies the number of glyphs in the set of glyphs used to form the font outline display lists. The <b>wglUseFontOutlines</b> function creates <i>count</i> display lists, one display list for each glyph in a set of glyphs.

### -param unnamedParam4

Specifies a starting display list.

### -param unnamedParam5

Specifies the maximum chordal deviation from the original outlines. When deviation is zero, the chordal deviation is equivalent to one design unit of the original font. The value of <i>deviation</i> must be equal to or greater than 0.

### -param unnamedParam6

Specifies how much a font is extruded in the negative <i>z</i> direction. The value must be equal to or greater than 0. When <i>extrusion</i> is 0, the display lists are not extruded.

### -param unnamedParam7

Specifies the format, either WGL_FONT_LINES or WGL_FONT_POLYGONS, to use in the display lists. When <i>format</i> is WGL_FONT_LINES, the <b>wglUseFontOutlines</b> function creates fonts with line segments. When <i>format</i> is WGL_FONT_POLYGONS, <b>wglUseFontOutlines</b> creates fonts with polygons.

### -param unnamedParam8

Points to an array of <i>count</i><a href="/windows/desktop/api/wingdi/ns-wingdi-glyphmetricsfloat">GLYPHMETRICSFLOAT</a> structures that is to receive the metrics of the glyphs. When <i>lpgmf</i> is <b>NULL</b>, no glyph metrics are returned.

## -returns

When the function succeeds, the return value is <b>TRUE</b>.

When the function fails, the return value is <b>FALSE</b> and no display lists are generated. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>wglUseFontOutlines</b> function defines the glyphs of an outline font with display lists in the current rendering context. The <b>wglUseFontOutlines</b> function works with TrueType fonts only; stroke and raster fonts are not supported.

Each display list consists of either line segments or polygons, and has a unique identifying number starting with the <i>listBase</i> number.

The <b>wglUseFontOutlines</b> function approximates glyph outlines by subdividing the quadratic B-spline curves of the outline into line segments, until the distance between the outline and the interpolated midpoint is within the value specified by <i>deviation</i>. This is the final format used when <i>format</i> is WGL_FONT_LINES. When you specify WGL_FONT_OUTLINES, the display lists created don't contain any normals; thus lighting doesn't work properly. To get the correct lighting of lines use WGL_FONT_POLYGONS and set <b>glPolygonMode</b>( GL_FRONT, GL_LINE ). When you specify <i>format</i> as WGL_FONT_POLYGONS the outlines are further tessellated into separate triangles, triangle fans, triangle strips, or quadrilateral strips to create the surface of each glyph. With WGL_FONT_POLYGONS, the created display lists call <b>glFrontFace</b>( GL_CW ) or <b>glFrontFace</b>( GL_CCW ); thus the current front-face value might be altered. For the best appearance of text with WGL_FONT_POLYGONS, cull the back faces as follows:


```cpp
glCullFace(GL_BACK); 
glEnable(GL_CULL_FACE);
```


A <b>GLYPHMETRICSFLOAT</b> structure contains information about the placement and orientation of each glyph in a character cell. The <i>lpgmf</i> parameter is an array of <b>GLYPHMETRICSFLOAT</b> structures holding the entire set of glyphs for a font. Each display list ends with a translation specified with the <b>gmfCellIncX</b> and <b>gmfCellIncY</b> members of the corresponding <b>GLYPHMETRICSFLOAT</b> structure. The translation enables the drawing of successive characters in their natural direction with a single call to <a href="/windows/desktop/OpenGL/glcalllists">glCallLists</a>.

<div class="alert"><b>Note</b>  With OpenGL for Windows, you cannot make GDI calls to a device context when a pixel format is double-buffered. You can work around this limitation by using <b>wglUseFontOutlines</b> and <a href="/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa">wglUseFontBitmaps</a>, when using double-buffered device contexts.</div>
<div> </div>

#### Examples

The following code example shows how to draw text using <b>wglUseFontOutlines</b>.


```cpp
HDC    hdc;  // A TrueType font has already been selected  
HGLRC  hglrc; 
GLYPHMETRICSFLOAT agmf[256]; 
 
// Make hglrc the calling thread's current rendering context  
wglMakeCurrent(hdc, hglrc); 
 
// create display lists for glyphs 0 through 255 with 0.1 extrusion  
// and default deviation. The display list numbering starts at 1000  
// (it could be any number)  
wglUseFontOutlines(hdc, 0, 255, 1000, 0.0f, 0.1f,  
            WGL_FONT_POLYGONS, &agmf); 
 
// Set up transformation to draw the string  
glLoadIdentity(); 
glTranslate(0.0f, 0.0f, -5.0f) 
glScalef(2.0f, 2.0f, 2.0f); 
 
// Display a string  
glListBase(1000); // Indicates the start of display lists for the glyphs  
// Draw the characters in a string  
glCallLists(24, GL_UNSIGNED_BYTE, "Hello Windows OpenGL World.");
```






> [!NOTE]
> The wingdi.h header defines wglUseFontOutlines as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-glyphmetricsfloat">GLYPHMETRICSFLOAT</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/OpenGL/glcalllists">glCallLists</a>



<a href="/windows/desktop/OpenGL/gllistbase">glListBase</a>



<a href="/windows/desktop/OpenGL/gltexgen-functions">glTexGen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa">wglUseFontBitmaps</a>
