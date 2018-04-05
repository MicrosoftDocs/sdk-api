---
UID: NF:gl.glReadPixels
title: glReadPixels function
author: windows-driver-content
description: The glReadPixels function reads a block of pixels from the framebuffer.
old-location: opengl\glreadpixels.htm
old-project: OpenGL
ms.assetid: 41fbad5c-b8ca-456d-bbfc-b48c176e15b0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_COLOR_INDEX, GL_DEPTH_COMPONENT, GL_RED, GL_GREEN, GL_BLUE, GL_ALPHA, GL_RGB, GL_RGBA, GL_BGR_EXT, GL_BGRA_EXT, GL_LUMINANCE, GL_LUMINANCE_ALPHA, GL_STENCIL_INDEX, _ogl_glReadPixels, gl/glReadPixels, glReadPixels, glReadPixels function [OpenGL], opengl.glreadpixels
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gl.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	opengl32.dll
api_name:
-	glReadPixels
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glReadPixels function


## -description


The <b>glReadPixels</b> function reads a block of pixels from the framebuffer.


## -parameters




### -param x

The window <i>x</i> coordinate of the first pixel that is read from the framebuffer. Together with the <i>y</i> coordinate, specifies the location of the lower-left corner of a rectangular block of pixels.


### -param y

The window <i>y</i> coordinates of the first pixel that is read from the framebuffer. Together with the <i>x</i> coordinate, specifies the location of the lower-left corner of a rectangular block of pixels.


### -param width

The width of the pixel rectangle.


### -param height

The height of the pixel rectangle. <i>Width</i> and <i>height</i> parameters of value "1" correspond to a single pixel.


### -param format

The format of the pixel data. The following symbolic values are accepted:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_INDEX"></a><a id="gl_color_index"></a><dl>
<dt><b>GL_COLOR_INDEX</b></dt>
</dl>
</td>
<td width="60%">
Color indexes are read from the color buffer selected by <a href="https://msdn.microsoft.com/734153fa-e809-4b70-867e-55e46ab95712">glReadBuffer</a>. Each index is converted to fixed point, shifted left or right, depending on the value and sign of GL_INDEX_SHIFT, and added to GL_INDEX_OFFSET. If GL_MAP_COLOR is GL_TRUE, indexes are replaced by their mappings in the table GL_PIXEL_MAP_I_TO_I.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_INDEX"></a><a id="gl_stencil_index"></a><dl>
<dt><b>GL_STENCIL_INDEX</b></dt>
</dl>
</td>
<td width="60%">
Stencil values are read from the stencil buffer. Each index is converted to fixed point, shifted left or right, depending on the value and sign of GL_INDEX_SHIFT, and added to GL_INDEX_OFFSET. If GL_MAP_STENCIL is GL_TRUE, indexes are replaced by their mappings in the table GL_PIXEL_MAP_S_TO_S.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_COMPONENT"></a><a id="gl_depth_component"></a><dl>
<dt><b>GL_DEPTH_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
Depth values are read from the depth buffer. Each component is converted to floating point such that the minimum depth value maps to 0.0 and the maximum value maps to 1.0. Each component is then multiplied by GL_DEPTH_SCALE, added to GL_DEPTH_BIAS, and finally clamped to the range [0,1].

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RED__GL_GREEN__GL_BLUE__GL_ALPHA__GL_RGB__GL_RGBA__GL_BGR_EXT__GL_BGRA_EXT__GL_LUMINANCE__GL_LUMINANCE_ALPHA"></a><a id="gl_red__gl_green__gl_blue__gl_alpha__gl_rgb__gl_rgba__gl_bgr_ext__gl_bgra_ext__gl_luminance__gl_luminance_alpha"></a><dl>
<dt><b>GL_RED, GL_GREEN, GL_BLUE, GL_ALPHA, GL_RGB, GL_RGBA, GL_BGR_EXT, GL_BGRA_EXT, GL_LUMINANCE, GL_LUMINANCE_ALPHA</b></dt>
</dl>
</td>
<td width="60%">
Processing differs depending on whether color buffers store color indexes or RGBA color components. If color indexes are stored, they are read from the color buffer selected by <a href="https://msdn.microsoft.com/734153fa-e809-4b70-867e-55e46ab95712">glReadBuffer</a>. Each index is converted to fixed point, shifted left or right, depending on the value and sign of GL_INDEX_SHIFT, and added to GL_INDEX_OFFSET. Indexes are then replaced by the red, green, blue, and alpha values obtained by indexing the GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B, and GL_PIXEL_MAP_I_TO_A tables. If RGBA color components are stored in the color buffers, they are read from the color buffer selected by <b>glReadBuffer</b>. Each color component is converted to floating point such that zero intensity maps to 0.0 and full intensity maps to 1.0. Each component is then multiplied by GL_c_SCALE and added to GL_c_BIAS, where c is GL_RED, GL_GREEN, GL_BLUE, and GL_ALPHA. Each component is clamped to the range [0,1]. Finally, if GL_MAP_COLOR is GL_TRUE, each color component c is replaced by its mapping in the table GL_PIXEL_MAP_c_TO_c, where c again is GL_RED, GL_GREEN, GL_BLUE, and GL_ALPHA. Each component is scaled to the size of its corresponding table before the lookup is performed. Finally, unneeded data is discarded. For example, GL_RED discards the green, blue, and alpha components, while GL_RGB discards only the alpha component. GL_LUMINANCE computes a single component value as the sum of the red, green, and blue components, and GL_LUMINANCE_ALPHA does the same, while keeping alpha as a second value.

</td>
</tr>
</table>
 


### -param type

The data type of the pixel data. Must be one of the following values.

<table>
<tr>
<th>Type</th>
<th>Index mask</th>
<th>Component conversion</th>
</tr>
<tr>
<td>GL_UNSIGNED_BYTE</td>
<td>2⁸1</td>
<td>(2⁸1)<i>c</i></td>
</tr>
<tr>
<td>GL_BYTE</td>
<td>2⁷1</td>
<td>[(2⁷1)<i>c</i>-1]/2</td>
</tr>
<tr>
<td>GL_BITMAP</td>
<td>1</td>
<td>1</td>
</tr>
<tr>
<td>GL_UNSIGNED_SHORT</td>
<td>2¹⁶1</td>
<td>(2¹⁶1)<i>c</i></td>
</tr>
<tr>
<td>GL_SHORT</td>
<td>2¹⁵1</td>
<td>[(2¹⁵1)<i>c</i>1]/2</td>
</tr>
<tr>
<td>GL_UNSIGNED_INT_</td>
<td>2³²1</td>
<td>(2³²1)<i>c</i></td>
</tr>
<tr>
<td>GL_INT</td>
<td>2³¹ 1</td>
<td>[(2³¹1)<i>c</i>1]/2</td>
</tr>
<tr>
<td>GL_FLOAT</td>
<td>none</td>
<td><i>c</i></td>
</tr>
</table>
 


### -param pixels

Returns the pixel data.


## -returns



This function does not return a value.




## -remarks



The <b>glReadPixels</b> function returns pixel data from the framebuffer, starting with the pixel whose lower-left corner is at location (<i>x</i>, <i>y</i>), into client memory starting at location <i>pixels</i>. Several parameters control the processing of the pixel data before it is placed into client memory. These parameters are set with three commands: <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>, <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>, and <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>. This topic describes the effects on <b>glReadPixels</b> of most, but not all of the parameters specified by these three commands.

The <b>glReadPixels</b> function returns values from each pixel with lower-left corner at (<i>x</i> + i, <i>y</i> + j) for 0 ≤ i &lt; <i>width</i> and 0 ≤ j &lt; <i>height</i>. This pixel is said to be the <i>i</i>th pixel in the <i>j</i>th row. Pixels are returned in row order from the lowest to the highest row, left to right in each row.

The shift, scale, bias, and lookup factors described above are all specified by <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>. The lookup table contents are specified by <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

The final step involves converting the indexes or components to the proper format, as specified by <i>type</i>. If <i>format</i> is GL_COLOR_INDEX or GL_STENCIL_INDEX and <i>type</i> is not GL_FLOAT, each index is masked with the mask value given in the following table. If <i>type</i> is GL_FLOAT, then each integer index is converted to single-precision floating-point format.

If <i>format</i> is GL_RED, GL_GREEN, GL_BLUE, GL_ALPHA, GL_RGB, GL_RGBA, GL_BGR_EXT, GL_BGRA_EXT, GL_LUMINANCE, or GL_LUMINANCE_ALPHA and <i>type</i> is not GL_FLOAT, each component is multiplied by the multiplier shown in the preceding table. If type is GL_FLOAT, then each component is passed as is (or converted to the client's single-precision floating-point format if it is different from the one used by OpenGL).

Return values are placed in memory as follows. If <i>format</i> is GL_COLOR_INDEX, GL_STENCIL_INDEX, GL_DEPTH_COMPONENT, GL_RED, GL_GREEN, GL_BLUE, GL_ALPHA, or GL_LUMINANCE, a single value is returned and the data for the <i>i</i>th pixel in the <i>j</i>th row is placed in location (<i>j</i> )<i>width</i> + <i>i</i>. GL_RGB and GL_BGR_EXT return three values, GL_RGBA and GL_BGRA_EXT return four values, and GL_LUMINANCE_ALPHA returns two values for each pixel, with all values corresponding to a single pixel occupying contiguous space in <i>pixels</i>. Storage parameters set by <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>, such as GL_PACK_SWAP_BYTES and GL_PACK_LSB_FIRST, affect the way that data is written into memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a> for a description.

Values for pixels that lie outside the window connected to the current OpenGL context are undefined.

If an error is generated, no change is made to the contents of <i>pixels</i>.

The following function retrieves information related to <b>glReadPixels</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_INDEX_MODE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/734153fa-e809-4b70-867e-55e46ab95712">glReadBuffer</a>
 

 

