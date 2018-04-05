---
UID: NF:glu.gluBuild1DMipmaps
title: gluBuild1DMipmaps function
author: windows-driver-content
description: The gluBuild1DMipmaps function creates 1-D mipmaps.
old-location: opengl\glubuild1dmipmaps.htm
old-project: OpenGL
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluBuild1DMipmaps, glu/gluBuild1DMipmaps, gluBuild1DMipmaps, gluBuild1DMipmaps function [OpenGL], opengl.glubuild1dmipmaps"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: glu.h
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
-	glu32.dll
api_name:
-	gluBuild1DMipmaps
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluBuild1DMipmaps function


## -description


The <b>gluBuild1DMipmaps</b> function creates 1-D mipmaps.


## -parameters




### -param target

The target texture. Must be GL_TEXTURE_1D.


### -param components

The number of color components in the texture. Must be 1, 2, 3, or 4.


### -param width

The width of the texture image.


### -param format

The format of the pixel data. The following values are valid: GL_COLOR_INDEX, GL_RED, GL_GREEN, GL_BLUE, GL_ALPHA, GL_RGB, GL_RGBA, GL_BGR_EXT, GL_BGRA_EXT, GL_LUMINANCE, or GL_LUMINANCE_ALPHA.


### -param type

The data type for <i>data</i>. The following values are valid: GL_UNSIGNED_BYTE, GL_BYTE, GL_BITMAP, GL_UNSIGNED_SHORT, GL_SHORT, GL_UNSIGNED_INT, GL_INT, or GL_FLOAT.


### -param data

A pointer to the image data in memory.


## -returns



This function does not return a value.




## -remarks



The <b>gluBuild1DMipmaps</b> function obtains the input image and generates all mipmap images (using <a href="https://msdn.microsoft.com/f47191e8-b22d-4f6a-949a-9c7782d6d338">gluScaleImage</a>) so that the input image can be used as a mipmapped texture image. The <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> function is then called to load each of the images. If the width of the input image is not a power of two, then the image is scaled to the nearest power of two before the mipmaps are generated.

A return value of zero indicates success. Otherwise, a GLU error code is returned (see <a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a>).

For a description of the acceptable values for the <i>format</i> parameter, see <b>glTexImage1D</b>. For a description of the acceptable values for the <i>type</i> parameter, see <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/ea19a9b0-baf7-436f-afd5-609bc364b3ba">gluBuild2DMipmaps</a>



<a href="https://msdn.microsoft.com/f47191e8-b22d-4f6a-949a-9c7782d6d338">gluScaleImage</a>
 

 

