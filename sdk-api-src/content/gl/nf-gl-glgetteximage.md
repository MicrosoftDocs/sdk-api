---
UID: NF:gl.glGetTexImage
title: glGetTexImage function
author: windows-driver-content
description: The glGetTexImage function returns a texture image.
old-location: opengl\glgetteximage.htm
old-project: OpenGL
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glGetTexImage, gl/glGetTexImage, glGetTexImage, glGetTexImage function [OpenGL], opengl.glgetteximage"
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
-	glGetTexImage
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetTexImage function


## -description


The <b>glGetTexImage</b> function returns a texture image.


## -parameters




### -param target

Specifies which texture is to be obtained. GL_TEXTURE_1D and GL_TEXTURE_2D are accepted.


### -param level

The level-of-detail number of the desired image. Level 0 is the base image level. Level <i>n</i> is the <i>n</i>th mipmap reduction image.


### -param format

A pixel format for the returned data. The supported formats are GL_RED, GL_GREEN, GL_BLUE, GL_ALPHA, GL_RGB, GL_RGBA, GL_LUMINANCE, GL_BGR_EXT, GL_BGRA_EXT, and GL_LUMINANCE_ALPHA.


### -param type

A pixel type for the returned data. The supported types are GL_UNSIGNED_BYTE, GL_BYTE, GL_UNSIGNED_SHORT, GL_SHORT, GL_UNSIGNED_INT, GL_INT, and GL_FLOAT.


### -param pixels

Returns the texture image. Should be a pointer to an array of the type specified by <i>type</i>.


## -returns



This function does not return a value.




## -remarks



The <b>glGetTexImage</b> function returns a texture image into <i>pixels</i>. The <i>target</i> parameter specifies whether the desired texture image is one specified by <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a><b>(</b>GL_TEXTURE_1D<b>)</b> or by <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a><b>(</b>GL_TEXTURE_2D<b>)</b>. The <i>level</i> parameter specifies the level-of-detail number of the desired image. The <i>format</i> and <i>type</i> parameters specify the format and type of the desired image array. For a description of the acceptable values for the <i>format</i> and <i>type</i> parameters, respectively, see <b>glTexImage1D</b> and <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>.

Operation of <b>glGetTexImage</b> is best understood by considering the selected internal four-component texture image to be an RGBA color buffer the size of the image. The semantics of <b>glGetTexImage</b> are then identical to those of <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a> called with the same <i>format</i> and <i>type</i>, with <i>x</i> and <i>y</i> set to zero, <i>width</i> set to the width of the texture image (including border if one was specified), and <i>height</i> set to one for 1-D images, or to the height of the texture image (including border, if one was specified) for 2-D images.

Because the internal texture image is an RGBA image, pixel formats GL_COLOR_INDEX, GL_STENCIL_INDEX, and GL_DEPTH_COMPONENT are not accepted, and pixel type GL_BITMAP is not accepted.

If the selected texture image does not contain four components, the following mappings are applied. Single-component textures are treated as RGBA buffers with red set to the single-component value, and green, blue, and alpha set to zero.

Two-component textures are treated as RGBA buffers, with red set to the value of component zero, alpha set to the value of component one, and green and blue set to zero. Finally, three-component textures are treated as RGBA buffers with red set to component zero, green set to component one, blue set to component two, and alpha set to zero.

To determine the required size of <i>pixels</i>, use <a href="https://msdn.microsoft.com/04aa02ef-5c9a-4b8a-a77f-fd5985c76fe2">glGetTexLevelParameter</a> to ascertain the dimensions of the internal texture image, and then scale the required number of pixels by the storage required for each pixel, based on <i>format</i> and <i>type</i>. Be sure to take the pixel-storage parameters into account, especially GL_PACK_ALIGNMENT.

If an error is generated, no change is made to the contents of <i>pixels</i>.

The following functions retrieve information related to <b>glGetTexImage</b>:
		


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_PACK_ALIGNMENT and others


<a href="https://msdn.microsoft.com/04aa02ef-5c9a-4b8a-a77f-fd5985c76fe2">glGetTexLevelParameter</a> with argument GL_TEXTURE_WIDTH

<b>glGetTexLevelParameter</b> with argument GL_TEXTURE_HEIGHT

<b>glGetTexLevelParameter</b> with argument GL_TEXTURE_BORDER

<b>glGetTexLevelParameter</b> with argument GL_TEXTURE_COMPONENTS




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/04aa02ef-5c9a-4b8a-a77f-fd5985c76fe2">glGetTexLevelParameter</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>
 

 

