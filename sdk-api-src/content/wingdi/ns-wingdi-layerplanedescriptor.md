---
UID: NS:wingdi.tagLAYERPLANEDESCRIPTOR
title: LAYERPLANEDESCRIPTOR (wingdi.h)
description: The LAYERPLANEDESCRIPTOR structure describes the pixel format of a drawing surface.
helpviewer_keywords: ["*LPLAYERPLANEDESCRIPTOR","*PLAYERPLANEDESCRIPTOR","LAYERPLANEDESCRIPTOR","LAYERPLANEDESCRIPTOR structure [OpenGL]","PLAYERPLANEDESCRIPTOR","PLAYERPLANEDESCRIPTOR structure pointer [OpenGL]","_ogl_LAYERPLANEDESCRIPTOR","opengl.layerplanedescriptor","wingdi/LAYERPLANEDESCRIPTOR","wingdi/PLAYERPLANEDESCRIPTOR"]
old-location: opengl\layerplanedescriptor.htm
tech.root: OpenGL
ms.assetid: fdb0322d-503f-4c17-b438-f764d60da7f6
ms.date: 12/05/2018
ms.keywords: '*LPLAYERPLANEDESCRIPTOR, *PLAYERPLANEDESCRIPTOR, LAYERPLANEDESCRIPTOR, LAYERPLANEDESCRIPTOR structure [OpenGL], PLAYERPLANEDESCRIPTOR, PLAYERPLANEDESCRIPTOR structure pointer [OpenGL], _ogl_LAYERPLANEDESCRIPTOR, opengl.layerplanedescriptor, wingdi/LAYERPLANEDESCRIPTOR, wingdi/PLAYERPLANEDESCRIPTOR'
req.header: wingdi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LAYERPLANEDESCRIPTOR, *PLAYERPLANEDESCRIPTOR, *LPLAYERPLANEDESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLAYERPLANEDESCRIPTOR
 - wingdi/tagLAYERPLANEDESCRIPTOR
 - PLAYERPLANEDESCRIPTOR
 - wingdi/PLAYERPLANEDESCRIPTOR
 - LAYERPLANEDESCRIPTOR
 - wingdi/LAYERPLANEDESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - LAYERPLANEDESCRIPTOR
---

# LAYERPLANEDESCRIPTOR structure


## -description

The <b>LAYERPLANEDESCRIPTOR</b> structure describes the pixel format of a drawing surface.

## -struct-fields

### -field nSize

Specifies the size of this data structure. Set this value to <b>sizeof</b>(<b>LAYERPLANEDESCRIPTOR</b>).

### -field nVersion

Specifies the version of this data structure. Set this value to 1.

### -field dwFlags

A set of bit flags that specify properties of the layer plane. The properties are generally not mutually exclusive; any combination of bit flags can be set, with the exceptions noted. The following bit flag constants are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>LPD_SUPPORT_OPENGL</td>
<td>The layer plane supports OpenGL drawing.</td>
</tr>
<tr>
<td>LPD_SUPPORT_GDI</td>
<td>The layer plane supports GDI drawing. The current implementation of OpenGL doesn't support this flag.</td>
</tr>
<tr>
<td>LPD_DOUBLEBUFFER</td>
<td>The layer plane is double-buffered. A layer plane can be double-buffered even when the main plane is single-buffered and vice versa.</td>
</tr>
<tr>
<td>LPD_STEREO</td>
<td>The layer plane is stereoscopic. A layer plane can be stereoscopic even when the main plane is monoscopic and vice versa.</td>
</tr>
<tr>
<td>LPD_SWAP_EXCHANGE</td>
<td>In a double-buffered layer plane, swapping the color buffer exchanges the front buffer and back buffer contents. The back buffer then contains the contents of the front buffer before the swap. This flag is a hint only and might not be provided by a driver.</td>
</tr>
<tr>
<td>LPD_SWAP_COPY</td>
<td>In a double-buffered layer plane, swapping the color buffer copies the back buffer contents to the front buffer. The swap does not affect the back buffer contents. This flag is a hint only and might not be provided by a driver.</td>
</tr>
<tr>
<td>LPD_TRANSPARENT</td>
<td>The <b>crTransparent</b> member of this structure contains a transparent color or index value that enables underlying layers to show through this layer. All layer planes, except the lowest-numbered underlay layer, have a transparent color or index.</td>
</tr>
<tr>
<td>LPD_SHARE_DEPTH</td>
<td>The layer plane shares the depth buffer with the main plane.</td>
</tr>
<tr>
<td>LPD_SHARE_STENCIL</td>
<td>The layer plane shares the stencil buffer with the main plane.</td>
</tr>
<tr>
<td>LPD_SHARE_ACCUM</td>
<td>The layer plane shares the accumulation buffer with the main plane.</td>
</tr>
</table>

### -field iPixelType

Specifies the type of pixel data. The following types are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>LPD_TYPE_RGBA</td>
<td>RGBA pixels. Each pixel has four components: red, green, blue, and alpha.</td>
</tr>
<tr>
<td>LPD_TYPE_COLORINDEX</td>
<td>Color-index pixels. Each pixel uses a color-index value.</td>
</tr>
</table>

### -field cColorBits

Specifies the number of color bitplanes in each color buffer. For RGBA pixel types, it is the size of the color buffer, excluding the alpha bitplanes. For color-index pixels, it is the size of the color-index buffer.

### -field cRedBits

Specifies the number of red bitplanes in each RGBA color buffer.

### -field cRedShift

Specifies the shift count for red bitplanes in each RGBA color buffer.

### -field cGreenBits

Specifies the number of green bitplanes in each RGBA color buffer.

### -field cGreenShift

Specifies the shift count for green bitplanes in each RGBA color buffer.

### -field cBlueBits

Specifies the number of blue bitplanes in each RGBA color buffer.

### -field cBlueShift

Specifies the shift count for blue bitplanes in each RGBA color buffer.

### -field cAlphaBits

Specifies the number of alpha bitplanes in each RGBA color buffer. Alpha bitplanes are not supported.

### -field cAlphaShift

Specifies the shift count for alpha bitplanes in each RGBA color buffer. Alpha bitplanes are not supported.

### -field cAccumBits

Specifies the total number of bitplanes in the accumulation buffer.

### -field cAccumRedBits

Specifies the number of red bitplanes in the accumulation buffer.

### -field cAccumGreenBits

Specifies the number of green bitplanes in the accumulation buffer.

### -field cAccumBlueBits

Specifies the number of blue bitplanes in the accumulation buffer.

### -field cAccumAlphaBits

Specifies the number of alpha bitplanes in the accumulation buffer.

### -field cDepthBits

Specifies the depth of the depth (z-axis) buffer.

### -field cStencilBits

Specifies the depth of the stencil buffer.

### -field cAuxBuffers

Specifies the number of auxiliary buffers. Auxiliary buffers are not supported.

### -field iLayerPlane

### -field bReserved

Not used. Must be zero.

### -field crTransparent

When the LPD_TRANSPARENT flag is set, specifies the transparent color or index value. Typically the value is zero.


#### - iLayerType

Specifies the layer plane number. Positive values of <b>iLayerType</b> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <b>PIXELFORMATDESCRIPTOR</b> structure.

## -remarks

Please notice, as documented above, that certain layer plane properties are not supported in the current implementation. The implementation is the Microsoft GDI software implementation of OpenGL. Hardware manufacturers that enhance parts of OpenGL may support some layer plane properties not supported by the generic implementation.

## -see-also

<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/structures">Structures</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext">wglCreateLayerContext</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane">wglDescribeLayerPlane</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries">wglGetLayerPaletteEntries</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette">wglRealizeLayerPalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries">wglSetLayerPaletteEntries</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers">wglSwapLayerBuffers</a>