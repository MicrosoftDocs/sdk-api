---
UID: NF:gl.glCopyTexSubImage2D
title: glCopyTexSubImage2D function
author: windows-driver-content
description: The glCopyTexSubImage2D function copies a sub-image of a two-dimensional texture image from the framebuffer.
old-location: opengl\glcopytexsubimage2d.htm
old-project: OpenGL
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glCopyTexSubImage2D, gl/glCopyTexSubImage2D, glCopyTexSubImage2D, glCopyTexSubImage2D function [OpenGL], opengl.glcopytexsubimage2d"
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
-	glCopyTexSubImage2D
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glCopyTexSubImage2D function


## -description


The <b>glCopyTexSubImage2D</b> function copies a sub-image of a two-dimensional texture image from the framebuffer.


## -parameters




### -param target

The target to which the image data will be changed. Must have the value GL_TEXTURE_2D.


### -param level

The level-of-detail number. Level 0 is the base image. Level <i>n</i> is the <i>n</i>th mipmap reduction image.


### -param xoffset

The texel offset in the <i>x</i> direction within the texture array.


### -param yoffset

The texel offset in the <i>y</i> direction within the texture array.


### -param x

The window x-plane coordinates of the lower-left corner of the row of pixels to be copied.


### -param y

The window y-plane coordinates of the lower-left corner of the row of pixels to be copied.


### -param width

The width of the sub-image of the texture image. Specifying a texture sub-image with zero width has no effect.


### -param height

The height of the sub-image of the texture image. Specifying a texture sub-image with zero width has no effect.


## -returns



This function does not return a value.




## -remarks



The <b>glCopyTexSubImage2D</b> function replaces a rectangular portion of a two-dimensional texture image with pixels from the current framebuffer, rather than from main memory as is the case for <a href="https://msdn.microsoft.com/2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7">glTexSubImage2D</a>.

A rectangle of pixels beginning with the <i>x</i> and <i>y</i> window coordinates and with the dimensions <i>width</i> and <i>height</i> replaces the portion of the texture array with the indexes <i>xoffset</i> through <i>xoffset</i> + (<i>width</i> - 1), with the indexes <i>yoffset</i> through <i>yoffset</i> + (<i>width</i> - 1) at the mipmap level specified by <i>level</i>. The destination rectangle in the texture array cannot include any texels outside the originally specified texture array.

The <b>glCopyTexSubImage2D</b> function processes the pixels in a row in the same way as <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>, except that before the final conversion of the pixels, all pixel component values are clamped to the range [0,1] and converted to the texture's internal format for storage in the texture array. Pixel ordering is determined with lower <i>x</i> coordinates corresponding to lower texture coordinates. If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.

If any of the pixels within the specified rectangle of the current framebuffer are outside the read window associated with the current rendering context, then the values obtained for those pixels are undefined. No change is made to the <i>internalFormat</i>, <i>width</i>, <i>height</i>, or <i>border</i> parameter of the specified texture array or to texel values outside the specified texture sub-image.

You cannot include calls to <b>glCopyTexSubImage2D</b> in display lists.

<div class="alert"><b>Note</b>  The <b>glCopyTexSubImage2D</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>
Texturing has no effect in color-index mode. The <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a> and <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a> functions affect texture images in exactly the way they affect the way pixels are drawn using <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>.

The following functions retrieve information related to <b>glCopyTexSubImage2D</b>:


<a href="https://msdn.microsoft.com/d7235df4-2dd8-4537-aadd-284c130a3f99">glGetTexImage</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_TEXTURE_2D




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/718aee8a-6dce-49e1-a441-19beccd89f8d">glCopyTexSubImage1D</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/80127d93-2aa8-420c-b05f-351ee29f202a">glTexParameter</a>



<a href="https://msdn.microsoft.com/2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7">glTexSubImage2D</a>
 

 

