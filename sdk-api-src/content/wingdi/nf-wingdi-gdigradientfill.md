---
UID: NF:wingdi.GdiGradientFill
title: GdiGradientFill function (wingdi.h)
description: The GdiGradientFill function fills rectangle and triangle structures.
helpviewer_keywords: ["GRADIENT_FILL_RECT_H","GRADIENT_FILL_RECT_V","GRADIENT_FILL_TRIANGLE","GdiGradientFill","GdiGradientFill function [Windows GDI]","gdi.gdigradientfill","wingdi/GdiGradientFill"]
old-location: gdi\gdigradientfill.htm
tech.root: gdi
ms.assetid: c88c1137-5690-4139-9d10-90d036e8f31c
ms.date: 12/05/2018
ms.keywords: GRADIENT_FILL_RECT_H, GRADIENT_FILL_RECT_V, GRADIENT_FILL_TRIANGLE, GdiGradientFill, GdiGradientFill function [Windows GDI], gdi.gdigradientfill, wingdi/GdiGradientFill
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GdiGradientFill
 - wingdi/GdiGradientFill
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GdiGradientFill
---

# GdiGradientFill function


## -description

The <b>GdiGradientFill</b> function fills rectangle and triangle structures.

## -parameters

### -param hdc [in]

A handle to the destination device context.

### -param pVertex [in]

A pointer to an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structures that each define a triangle vertex.

### -param nVertex [in]

The number of vertices in <i>pVertex</i>.

### -param pMesh [in]

An array of <a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_triangle">GRADIENT_TRIANGLE</a> structures in triangle mode, or an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_rect">GRADIENT_RECT</a> structures in rectangle mode.

### -param nCount [in]

The number of elements (triangles or rectangles) in <i>pMesh</i>.

### -param ulMode [in]

The gradient fill mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_RECT_H"></a><a id="gradient_fill_rect_h"></a><dl>
<dt><b>GRADIENT_FILL_RECT_H</b></dt>
</dl>
</td>
<td width="60%">
In this mode, two endpoints describe a rectangle. The rectangle is defined to have a constant color (specified by the <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structure) for the left and right edges. GDI interpolates the color from the left to right edge and fills the interior.

</td>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_RECT_V"></a><a id="gradient_fill_rect_v"></a><dl>
<dt><b>GRADIENT_FILL_RECT_V</b></dt>
</dl>
</td>
<td width="60%">
In this mode, two endpoints describe a rectangle. The rectangle is defined to have a constant color (specified by the <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structure) for the top and bottom edges. GDI interpolates the color from the top to bottom edge and fills the interior.

</td>
</tr>
<tr>
<td width="40%"><a id="GRADIENT_FILL_TRIANGLE"></a><a id="gradient_fill_triangle"></a><dl>
<dt><b>GRADIENT_FILL_TRIANGLE</b></dt>
</dl>
</td>
<td width="60%">
In this mode, an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structures is passed to GDI along with a list of array indexes that describe separate triangles. GDI performs linear interpolation between triangle vertices and fills the interior. Drawing is done directly in 24- and 32-bpp modes. Dithering is performed in 16-, 8-, 4-, and 1-bpp mode.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -remarks

<div class="alert"><b>Note</b>  This function is the same as <a href="/windows/desktop/api/wingdi/nf-wingdi-gradientfill">GradientFill</a>.</div>
<div> </div>
To add smooth shading to a triangle, call the <b>GdiGradientFill</b> function with the three triangle endpoints. GDI will linearly interpolate and fill the triangle. Here is the drawing output of a shaded triangle.

<img alt="Illustration of a triangle that fills from orange at the top point to magenta on the bottom line " border="0" src="./images/GradientFillTriangle.png"/>
To add smooth shading to a rectangle, call <b>GdiGradientFill</b> with the upper-left and lower-right coordinates of the rectangle. There are two shading modes used when drawing a rectangle. In horizontal mode, the rectangle is shaded from left-to-right. In vertical mode, the rectangle is shaded from top-to-bottom. Here is the drawing output of two shaded rectangles - one in horizontal mode, the other in vertical mode.

<img alt="Illustration of a rectangle that shades from dark on the left side to light on the right side" border="0" src="./images/GradientFillRectangle.png"/>
<img alt="Illustration of a rectangle that shades from dark on the top to light on the bottom" border="0" src="./images/GradientFillRectangle2.png"/>
The <b>GdiGradientFill</b> function uses a mesh method to specify the endpoints of the object to draw. All vertices are passed to <b>GdiGradientFill</b> in the <i>pVertex</i> array. The <i>pMesh</i> parameter specifies how these vertices are connected to form an object. When filling a rectangle, <i>pMesh</i> points to an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_rect">GRADIENT_RECT</a> structures. Each <b>GRADIENT_RECT</b> structure specifies the index of two vertices in the <i>pVertex</i> array. These two vertices form the upper-left and lower-right boundary of one rectangle.

In the case of filling a triangle, <i>pMesh</i> points to an array of <a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_triangle">GRADIENT_TRIANGLE</a> structures. Each <b>GRADIENT_TRIANGLE</b> structure specifies the index of three vertices in the <i>pVertex</i> array. These three vertices form one triangle.

To simplify hardware acceleration, this routine is not required to be pixel-perfect in the triangle interior.

Note that <b>GdiGradientFill</b> does not use the Alpha member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a> structure. To use <b>GdiGradientFill</b> with transparency, call <b>GdiGradientFill</b> and then call <a href="/windows/desktop/api/wingdi/nf-wingdi-gdialphablend">GdiAlphaBlend</a> with the desired values for the alpha channel of each vertex.

For more information, see <a href="/windows/desktop/gdi/smooth-shading">Smooth Shading</a>, <a href="/windows/desktop/gdi/drawing-a-shaded-triangle">Drawing a Shaded Triangle</a>, and <a href="/windows/desktop/gdi/drawing-a-shaded-rectangle">Drawing a Shaded Rectangle</a>.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-emrgradientfill">EMRGRADIENTFILL</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_rect">GRADIENT_RECT</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-gradient_triangle">GRADIENT_TRIANGLE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-trivertex">TRIVERTEX</a>