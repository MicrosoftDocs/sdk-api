---
UID: NF:gl.glTexSubImage1D
title: glTexSubImage1D function
author: windows-driver-content
description: The glTexSubImage1D function specifies a portion of an existing one-dimensional texture image. You cannot define a new texture with glTexSubImage1D.
old-location: opengl\gltexsubimage1d.htm
old-project: OpenGL
ms.assetid: e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ALPHA, GL_BLUE, GL_COLOR_INDEX, GL_GREEN, GL_LUMINANCE, GL_LUMINANCE_ALPHA, GL_RED, GL_RGB, GL_RGBA, _ogl_glTexSubImage1D, gl/glTexSubImage1D, glTexSubImage1D, glTexSubImage1D function [OpenGL], opengl.gltexsubimage1d
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
-	glTexSubImage1D
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glTexSubImage1D function


## -description


The <b>glTexSubImage1D</b> function specifies a portion of an existing one-dimensional texture image. You cannot define a new texture with <b>glTexSubImage1D</b>.


## -parameters




### -param target

The target texture. Must be GL_TEXTURE_1D.


### -param level

The level-of-detail number. Level 0 is the base image. Level <i>n</i> is the <i>n</i>th mipmap reduction image.


### -param xoffset

A texel offset in the <i>x</i> direction within the texture array.


### -param width

The width of the texture sub-image.


### -param format

The format of the pixel data. This parameter can assume one of the following symbolic values.

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
Each element is a single value, a color index. It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL_INDEX_SHIFT, and added to GL_INDEX_OFFSET (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>). The resulting index is converted to a set of color components using the GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B, and GL_PIXEL_MAP_I_TO_A tables, and clamped to the range [0,1].

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RED"></a><a id="gl_red"></a><dl>
<dt><b>GL_RED</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single red component. It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <b>glPixelTransfer</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GREEN"></a><a id="gl_green"></a><dl>
<dt><b>GL_GREEN</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single green component. It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLUE"></a><a id="gl_blue"></a><dl>
<dt><b>GL_BLUE</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single blue component. It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <b>glPixelTransfer</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA"></a><a id="gl_alpha"></a><dl>
<dt><b>GL_ALPHA</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single alpha component. It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>).

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
Each element is a complete RGBA element. It is converted to floating point format. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <b>glPixelTransfer</b>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LUMINANCE"></a><a id="gl_luminance"></a><dl>
<dt><b>GL_LUMINANCE</b></dt>
</dl>
</td>
<td width="60%">
Each element is a single luminance value. It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LUMINANCE_ALPHA"></a><a id="gl_luminance_alpha"></a><dl>
<dt><b>GL_LUMINANCE_ALPHA</b></dt>
</dl>
</td>
<td width="60%">
Each element is a luminance/alpha pair. It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue. Each component is then multiplied by the signed scale factor GL_c_SCALE, added to the signed bias GL_c_BIAS, and clamped to the range [0,1] (see <b>glPixelTransfer</b>).

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



One-dimensional texturing for a primitive is enabled using <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> with the argument GL_TEXTURE_1D. During texturing, part of a specified texture image is mapped into each enabled primitive. You use the <b>glTexSubImage1D</b> function to specify a contiguous sub-image of an existing one-dimensional texture image for texturing.

The texels referenced by <i>pixels</i> replace a region of the existing texture array with <i>x</i> indexes of <i>xoffset</i> and <i>xoffset</i> + (<i>width</i> 1) inclusive. This region cannot include any texels outside the range of the originally specified texture array.

Specifying a sub-image with a <i>width</i> of zero has no effect and does not generate an error.

Texturing has no effect in color-index mode.

In general, texture images can be represented by the same data formats as the pixels in a <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a> command, except that GL_STENCIL_INDEX and GL_DEPTH_COMPONENT cannot be used. The <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a> and <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a> modes affect texture images in exactly the way they affect <b>glDrawPixels</b>.

The following functions retrieve information related to <b>glTexSubImage1D</b>:


<a href="https://msdn.microsoft.com/d7235df4-2dd8-4537-aadd-284c130a3f99">glGetTexImage</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_TEXTURE_1D




## -see-also




<a href="https://msdn.microsoft.com/3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd">glCopyTexImage1D</a>



<a href="https://msdn.microsoft.com/4b9d7be6-054d-4590-b3f0-a2a670786c4b">glCopyTexImage2D</a>



<a href="https://msdn.microsoft.com/718aee8a-6dce-49e1-a441-19beccd89f8d">glCopyTexSubImage1D</a>



<a href="https://msdn.microsoft.com/cbb644d4-6a23-4d66-8599-5f8b48e9b91f">glCopyTexSubImage2D</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>



<a href="https://msdn.microsoft.com/d7235df4-2dd8-4537-aadd-284c130a3f99">glGetTexImage</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>



<a href="https://msdn.microsoft.com/2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7">glTexSubImage2D</a>
 

 

