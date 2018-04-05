---
UID: NF:gl.glTexImage2D
title: glTexImage2D function
author: windows-driver-content
description: The glTexImage2D function specifies a two-dimensional texture image.
old-location: opengl\glteximage2d.htm
old-project: OpenGL
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ALPHA, GL_BGRA_EXT, GL_BGR_EXT, GL_BLUE, GL_COLOR_INDEX, GL_GREEN, GL_LUMINANCE, GL_LUMINANCE_ALPHA, GL_RED, GL_RGB, GL_RGBA, _ogl_glTexImage2D, gl/glTexImage2D, glTexImage2D, glTexImage2D function [OpenGL], opengl.glteximage2d
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
-	glTexImage2D
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glTexImage2D function


## -description


The <b>glTexImage2D</b> function specifies a two-dimensional texture image.


## -parameters




### -param target

The target texture. Must be GL_TEXTURE_2D.


### -param level

The level-of-detail number. Level 0 is the base image level. Level <i>n</i> is the <i>n</i> th mipmap reduction image.


### -param internalformat

The number of color components in the texture. Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL_ALPHA, GL_ALPHA4, GL_ALPHA8, GL_ALPHA12, GL_ALPHA16, GL_LUMINANCE, GL_LUMINANCE4, GL_LUMINANCE8, GL_LUMINANCE12, GL_LUMINANCE16, GL_LUMINANCE_ALPHA, GL_LUMINANCE4_ALPHA4, GL_LUMINANCE6_ALPHA2, GL_LUMINANCE8_ALPHA8, GL_LUMINANCE12_ALPHA4, GL_LUMINANCE12_ALPHA12, GL_LUMINANCE16_ALPHA16, GL_INTENSITY, GL_INTENSITY4, GL_INTENSITY8, GL_INTENSITY12, GL_INTENSITY16, GL_R3_G3_B2, GL_RGB, GL_RGB4, GL_RGB5, GL_RGB8, GL_RGB10, GL_RGB12, GL_RGB16, GL_RGBA, GL_RGBA2, GL_RGBA4, GL_RGB5_A1, GL_RGBA8, GL_RGB10_A2, GL_RGBA12, or GL_RGBA16.


### -param width

The width of the texture image. Must be 2<i>ⁿ</i> + 2(<i>border</i>) for some integer <i>n</i>.


### -param height

The height of the texture image. Must be 2<i><sup>m</sup></i> + 2(<i>border</i>) for some integer <i>m</i>.


### -param border

The width of the border. Must be either 0 or 1.


### -param format

The format of the pixel data. It can assume one of nine symbolic values.

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
Each element is a single value, a color index. It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right depending on the value and sign of GL_INDEX_SHIFT, and added to GL_INDEX_OFFSET (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>). The resulting index is converted to a set of color components using the GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B, and GL_PIXEL_MAP_I_TO_A tables, and clamped to the range [0,1].

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RED"></a><a id="gl_red"></a><dl>
<dt><b>GL_RED</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single red component. It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <b>glPixelTransfer</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GREEN"></a><a id="gl_green"></a><dl>
<dt><b>GL_GREEN</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single green component. It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLUE"></a><a id="gl_blue"></a><dl>
<dt><b>GL_BLUE</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single blue component. It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <b>glPixelTransfer</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA"></a><a id="gl_alpha"></a><dl>
<dt><b>GL_ALPHA</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single red component. It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RGB"></a><a id="gl_rgb"></a><dl>
<dt><b>GL_RGB</b></dt>
</dl>
</td>
<td width="60%">
Each element is an RGB triple. It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <b>glPixelTransfer</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RGBA"></a><a id="gl_rgba"></a><dl>
<dt><b>GL_RGBA</b></dt>
</dl>
</td>
<td width="60%">
Each element is a complete RGBA element. It is converted to floating point. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BGR_EXT"></a><a id="gl_bgr_ext"></a><dl>
<dt><b>GL_BGR_EXT</b></dt>
</dl>
</td>
<td width="60%">
Each pixel is a group of three components in this order: blue, green, red.

GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs). Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BGRA_EXT"></a><a id="gl_bgra_ext"></a><dl>
<dt><b>GL_BGRA_EXT</b></dt>
</dl>
</td>
<td width="60%">
Each pixel is a group of four components in this order: blue, green, red, alpha. GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs). Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LUMINANCE"></a><a id="gl_luminance"></a><dl>
<dt><b>GL_LUMINANCE</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single luminance value. It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <b>glPixelTransfer</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LUMINANCE_ALPHA"></a><a id="gl_luminance_alpha"></a><dl>
<dt><b>GL_LUMINANCE_ALPHA</b></dt>
</dl>
</td>
<td width="60%">
Each element is a luminance/alpha pair. It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>).

</td>
</tr>
</table>
 


### -param type

The data type of the pixel data. The following symbolic values are accepted: GL_UNSIGNED_BYTE, GL_BYTE, GL_BITMAP, GL_UNSIGNED_SHORT, GL_SHORT, GL_UNSIGNED_INT, GL_INT, and GL_FLOAT.


### -param pixels

A pointer to the image data in memory.


## -returns



This function does not return a value.




## -remarks



The <b>glTexImage2D</b> function specifies a two-dimensional texture image. Texturing maps a portion of a specified <i>texture image</i> onto each graphical primitive for which texturing is enabled. Two-dimensional texturing is enabled and disabled using <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> with argument GL_TEXTURE_2D.

Texture images are defined with <b>glTexImage2D</b>. The arguments describe the parameters of the texture image, such as height, width, width of the border, level-of-detail number (see <a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>), and number of color components provided. The last three arguments describe the way the image is represented in memory. These arguments are identical to the pixel formats used for <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>.

Data is read from <i>pixels</i> as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on <i>type</i>. These values are grouped into sets of one, two, three, or four values, depending on <i>format</i>, to form elements. If <i>type</i> is GL_BITMAP, the data is considered as a string of unsigned bytes (and <i>format</i> must be GL_COLOR_INDEX). Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL_UNPACK_LSB_FIRST (see <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>). Please see <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a> for a description of the acceptable values for the <i>type</i> parameter.

A texture image can have up to four components per texture element, depending on <i>components</i>. A one-component texture image uses only the red component of the RGBA color extracted from <i>pixels</i>. A two-component image uses the R and A values. A three-component image uses the R, G, and B values. A four-component image uses all of the RGBA components.

Texturing has no effect in color-index mode.

The texture image can be represented by the same data formats as the pixels in a <b>glDrawPixels</b> command, except that GL_STENCIL_INDEX and GL_DEPTH_COMPONENT cannot be used. The <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a> and <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a> modes affect texture images in exactly the way they affect <b>glDrawPixels</b>.

A texture image with zero height or width indicates the null texture. If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.

The following functions retrieve information related to <b>glTexImage2D</b>:


<a href="https://msdn.microsoft.com/d7235df4-2dd8-4537-aadd-284c130a3f99">glGetTexImage</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_TEXTURE_2D




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

