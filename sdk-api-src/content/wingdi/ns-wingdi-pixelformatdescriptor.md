---
UID: NS:wingdi.tagPIXELFORMATDESCRIPTOR
title: PIXELFORMATDESCRIPTOR (wingdi.h)
author: windows-sdk-content
description: The PIXELFORMATDESCRIPTOR structure describes the pixel format of a drawing surface.
old-location: opengl\pixelformatdescriptor.htm
tech.root: OpenGL
ms.assetid: 1480dea3-ae74-4e8b-b4de-fca8de5d8395
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPPIXELFORMATDESCRIPTOR, *PPIXELFORMATDESCRIPTOR, PIXELFORMATDESCRIPTOR, PIXELFORMATDESCRIPTOR structure [OpenGL], PPIXELFORMATDESCRIPTOR, PPIXELFORMATDESCRIPTOR structure pointer [OpenGL], _ogl_PIXELFORMATDESCRIPTOR, opengl.pixelformatdescriptor, wingdi/PIXELFORMATDESCRIPTOR, wingdi/PPIXELFORMATDESCRIPTOR"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - PIXELFORMATDESCRIPTOR
product: Windows
targetos: Windows
req.typenames: PIXELFORMATDESCRIPTOR, *PPIXELFORMATDESCRIPTOR, *LPPIXELFORMATDESCRIPTOR
req.redist: 
---

# PIXELFORMATDESCRIPTOR structure


## -description



The <b>PIXELFORMATDESCRIPTOR</b> structure describes the pixel format of a drawing surface.




## -struct-fields




### -field nSize

Specifies the size of this data structure. This value should be set to <b>sizeof</b>(<b>PIXELFORMATDESCRIPTOR</b>).


### -field nVersion

Specifies the version of this data structure. This value should be set to 1.


### -field dwFlags

A set of bit flags that specify properties of the pixel buffer. The properties are generally not mutually exclusive; you can set any combination of bit flags, with the exceptions noted. The following bit flag constants are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PFD_DRAW_TO_WINDOW</td>
<td>The buffer can draw to a window or device surface.</td>
</tr>
<tr>
<td>PFD_DRAW_TO_BITMAP</td>
<td>The buffer can draw to a memory bitmap.</td>
</tr>
<tr>
<td>PFD_SUPPORT_GDI</td>
<td>The buffer supports GDI drawing. This flag and PFD_DOUBLEBUFFER are mutually exclusive in the current generic implementation.</td>
</tr>
<tr>
<td>PFD_SUPPORT_OPENGL</td>
<td>The buffer supports OpenGL drawing.</td>
</tr>
<tr>
<td>PFD_GENERIC_ACCELERATED</td>
<td>The pixel format is supported by a device driver that accelerates the generic implementation. If this flag is clear and the PFD_GENERIC_FORMAT flag is set, the pixel format is supported by the generic implementation only.</td>
</tr>
<tr>
<td>PFD_GENERIC_FORMAT</td>
<td>The pixel format is supported by the GDI software implementation, which is also known as the generic implementation. If this bit is clear, the pixel format is supported by a device driver or hardware.</td>
</tr>
<tr>
<td>PFD_NEED_PALETTE</td>
<td>The buffer uses RGBA pixels on a palette-managed device. A logical palette is required to achieve the best results for this pixel type. Colors in the palette should be specified according to the values of the <b>cRedBits</b>, <b>cRedShift</b>, <b>cGreenBits</b>, <b>cGreenShift</b>, <b>cBluebits</b>, and <b>cBlueShift</b> members. The palette should be created and realized in the device context before calling <a href="https://msdn.microsoft.com/a1d3cbc9-2587-4f49-9d7d-749cf9a3ecfe">wglMakeCurrent</a>.</td>
</tr>
<tr>
<td>PFD_NEED_SYSTEM_PALETTE</td>
<td>Defined in the pixel format descriptors of hardware that supports one hardware palette in 256-color mode only. For such systems to use hardware acceleration, the hardware palette must be in a fixed order (for example, 3-3-2) when in RGBA mode or must match the logical palette when in color-index mode.When this flag is set, you must call <b>SetSystemPaletteUse</b> in your program to force a one-to-one mapping of the logical palette and the system palette. If your OpenGL hardware supports multiple hardware palettes and the device driver can allocate spare hardware palettes for OpenGL, this flag is typically clear.

This flag is not set in the generic pixel formats.

</td>
</tr>
<tr>
<td>PFD_DOUBLEBUFFER</td>
<td>The buffer is double-buffered. This flag and PFD_SUPPORT_GDI are mutually exclusive in the current generic implementation.</td>
</tr>
<tr>
<td>PFD_STEREO</td>
<td>The buffer is stereoscopic. This flag is not supported in the current generic implementation.</td>
</tr>
<tr>
<td>PFD_SWAP_LAYER_BUFFERS</td>
<td>Indicates whether a device can swap individual layer planes with pixel formats that include double-buffered overlay or underlay planes. Otherwise all layer planes are swapped together as a group. When this flag is set, <b>wglSwapLayerBuffers</b> is supported.</td>
</tr>
</table>
 

You can specify the following bit flags when calling <a href="https://msdn.microsoft.com/17bd0a2c-5257-4ae3-80f4-a5ad536169fb">ChoosePixelFormat</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PFD_DEPTH_DONTCARE</td>
<td>The requested pixel format can either have or not have a depth buffer. To select a pixel format without a depth buffer, you must specify this flag. The requested pixel format can be with or without a depth buffer. Otherwise, only pixel formats with a depth buffer are considered.</td>
</tr>
<tr>
<td>PFD_DOUBLEBUFFER<div> </div>_DONTCARE</td>
<td>The requested pixel format can be either single- or double-buffered.</td>
</tr>
<tr>
<td>PFD_STEREO_DONTCARE</td>
<td>The requested pixel format can be either monoscopic or stereoscopic.</td>
</tr>
</table>
 

With the <b>glAddSwapHintRectWIN</b> extension function, two new flags are included for the <b>PIXELFORMATDESCRIPTOR</b> pixel format structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PFD_SWAP_COPY</td>
<td>Specifies the content of the back buffer in the double-buffered main color plane following a buffer swap. Swapping the color buffers causes the content of the back buffer to be copied to the front buffer. The content of the back buffer is not affected by the swap. PFD_SWAP_COPY is a hint only and might not be provided by a driver.</td>
</tr>
<tr>
<td>PFD_SWAP_EXCHANGE</td>
<td>Specifies the content of the back buffer in the double-buffered main color plane following a buffer swap. Swapping the color buffers causes the exchange of the back buffer's content with the front buffer's content. Following the swap, the back buffer's content contains the front buffer's content before the swap. PFD_SWAP_EXCHANGE is a hint only and might not be provided by a driver.</td>
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
<td>PFD_TYPE_RGBA</td>
<td>RGBA pixels. Each pixel has four components in this order: red, green, blue, and alpha.</td>
</tr>
<tr>
<td>PFD_TYPE_COLORINDEX</td>
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


### -field iLayerType

Ignored. Earlier implementations of OpenGL used this member, but it is no longer used.


### -field bReserved

Specifies the number of overlay and underlay planes. Bits 0 through 3 specify up to 15 overlay planes and bits 4 through 7 specify up to 15 underlay planes.


### -field dwLayerMask

Ignored. Earlier implementations of OpenGL used this member, but it is no longer used.


### -field dwVisibleMask

Specifies the transparent color or index of an underlay plane. When the pixel type is RGBA, <b>dwVisibleMask</b> is a transparent RGB color value. When the pixel type is color index, it is a transparent index value.


### -field dwDamageMask

Ignored. Earlier implementations of OpenGL used this member, but it is no longer used.


## -remarks



Please notice carefully, as documented above, that certain pixel format properties are not supported in the current generic implementation. The generic implementation is the Microsoft GDI software implementation of OpenGL. Hardware manufacturers may enhance parts of OpenGL, and may support some pixel format properties not supported by the generic implementation.




## -see-also




<a href="https://msdn.microsoft.com/17bd0a2c-5257-4ae3-80f4-a5ad536169fb">ChoosePixelFormat</a>



<a href="https://msdn.microsoft.com/9692a30d-c7d4-40c7-a265-72c4ebabd5f2">DescribePixelFormat</a>



<a href="https://msdn.microsoft.com/e9a65f3a-6932-462f-b342-a993d222fae8">GetPixelFormat</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a>



<a href="https://msdn.microsoft.com/109c41b1-d3d2-4c1d-9809-99a0a89df263">Structures</a>
 

 

