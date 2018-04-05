---
UID: NF:gl.glCopyTexImage1D
title: glCopyTexImage1D function
author: windows-driver-content
description: The glCopyTexImage1D function copies pixels from the framebuffer into a one-dimensional texture image.
old-location: opengl\glcopyteximage1d.htm
old-project: OpenGL
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glCopyTexImage1D, gl/glCopyTexImage1D, glCopyTexImage1D, glCopyTexImage1D function [OpenGL], opengl.glcopyteximage1d"
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
-	glCopyTexImage1D
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glCopyTexImage1D function


## -description


The <b>glCopyTexImage1D</b> function copies pixels from the framebuffer into a one-dimensional texture image.


## -parameters




### -param target

The target for which the image data will be changed. Must have the value GL_TEXTURE_1D.


### -param level

The level-of-detail number. Level 0 is the base image. Level <i>n</i> is the <i>n</i>th mipmap reduction image.


### -param internalFormat

The internal format and resolution of the texture data. This parameter must be one of the following symbolic values.

<table>
<tr>
<th>Constant</th>
<th>R Bits</th>
<th>G Bits</th>
<th>B Bits</th>
<th>A Bits</th>
<th>L Bits</th>
<th>I Bits</th>
</tr>
<tr>
<td>GL_ALPHA</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_ALPHA4</td>
<td></td>
<td></td>
<td></td>
<td>4</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_ALPHA8</td>
<td></td>
<td></td>
<td></td>
<td>8</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_ALPHA12</td>
<td></td>
<td></td>
<td></td>
<td>12</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_ALPHA16</td>
<td></td>
<td></td>
<td></td>
<td>16</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE4</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>4</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE8</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>8</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE12</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>12</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE16</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>16</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE_ALPHA</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE4_ALPHA4</td>
<td></td>
<td></td>
<td></td>
<td>4</td>
<td>4</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE6_ALPHA2</td>
<td></td>
<td></td>
<td></td>
<td>2</td>
<td>6</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE8_ALPHA8</td>
<td></td>
<td></td>
<td></td>
<td>8</td>
<td>8</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE12_ALPHA4</td>
<td></td>
<td></td>
<td></td>
<td>4</td>
<td>12</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE12_ALPHA12</td>
<td></td>
<td></td>
<td></td>
<td>12</td>
<td>12</td>
<td></td>
</tr>
<tr>
<td>GL_LUMINANCE16_ALPHA16</td>
<td></td>
<td></td>
<td></td>
<td>16</td>
<td>16</td>
<td></td>
</tr>
<tr>
<td>GL_INTENSITY</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_INTENSITY4</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>4</td>
</tr>
<tr>
<td>GL_INTENSITY8</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>8</td>
</tr>
<tr>
<td>GL_INTENSITY12</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>12</td>
</tr>
<tr>
<td>GL_INTENSITY16</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>16</td>
</tr>
<tr>
<td>GL_RGB</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_R3_G3_B2</td>
<td>3</td>
<td>3</td>
<td>2</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGB4</td>
<td>4</td>
<td>4</td>
<td>4</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGB5</td>
<td>5</td>
<td>5</td>
<td>5</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGB8</td>
<td>8</td>
<td>8</td>
<td>8</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGB10</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGB12</td>
<td>12</td>
<td>12</td>
<td>12</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGB16</td>
<td>16</td>
<td>16</td>
<td>16</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGBA</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGBA2</td>
<td>2</td>
<td>2</td>
<td>2</td>
<td>2</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGBA4</td>
<td>4</td>
<td>4</td>
<td>4</td>
<td>4</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGB5_A1</td>
<td>5</td>
<td>5</td>
<td>5</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGBA8</td>
<td>8</td>
<td>8</td>
<td>8</td>
<td>8</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGB10_A2</td>
<td>10</td>
<td>10</td>
<td>10</td>
<td>2</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGBA12</td>
<td>12</td>
<td>12</td>
<td>12</td>
<td>12</td>
<td></td>
<td></td>
</tr>
<tr>
<td>GL_RGBA16</td>
<td>16</td>
<td>16</td>
<td>16</td>
<td>16</td>
<td></td>
<td></td>
</tr>
</table>
 


### -param x

The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.


### -param y

The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.


### -param width

The width of the texture image. Must be zero or 2ⁿ + 2(<i>border</i>) for some integer <i>n</i>. The height of the texture image is 1.


### -param border

The width of the border. Must be either zero or 1.


## -returns



This function does not return a value.




## -remarks



The <b>glCopyTexImage1D</b> function defines a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>.

Using the mipmap level specified with <i>level</i>, texture arrays are defined as a pixel row aligned with the lower-left corner of the window at the coordinates specified by <i>x</i> and <i>y</i>, with a length equal to <i>width</i> + 2 * <i>border</i>. The internal format of the texture array is specified with the <i>internalFormat</i> parameter.

The <b>glCopyTexImage1D</b> function processes the pixels in a row in the same way as <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>, except that before the final conversion of the pixels, all pixel component values are clamped to the range [0,1] and converted to the texture's internal format for storage in the texture array. Pixel ordering is determined with lower <i>x</i> coordinates corresponding to lower texture coordinates. If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.

You cannot include calls to <b>glCopyTexImage1D</b> in display lists.

<div class="alert"><b>Note</b>  The <b>glCopyTexImage1D</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>
Texturing has no effect in color-index mode. The <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a> and <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a> functions affect texture images in exactly the way they affect <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>.

The following function retrieves information related to <b>glCopyTexImage1D</b>:


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_TEXTURE_1D




## -see-also




<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/4b9d7be6-054d-4590-b3f0-a2a670786c4b">glCopyTexImage2D</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>
 

 

