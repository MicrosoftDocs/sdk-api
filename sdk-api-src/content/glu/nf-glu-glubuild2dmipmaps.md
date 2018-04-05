---
UID: NF:glu.gluBuild2DMipmaps
title: gluBuild2DMipmaps function
author: windows-driver-content
description: The gluBuild2DMipmaps function creates 2-D mipmaps.
old-location: opengl\glubuild2dmipmaps.htm
old-project: OpenGL
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluBuild2DMipmaps, glu/gluBuild2DMipmaps, gluBuild2DMipmaps, gluBuild2DMipmaps function [OpenGL], opengl.glubuild2dmipmaps"
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
-	gluBuild2DMipmaps
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluBuild2DMipmaps function


## -description


The <b>gluBuild2DMipmaps</b> function creates 2-D mipmaps.


## -parameters




### -param target

The target texture. Must be GL_TEXTURE_2D.


### -param components

The number of color components in the texture. Must be 1, 2, 3, or 4.


### -param width

The width of the texture image.


### -param height

The height of the texture image.


### -param format

The format of the pixel data. Must be one of the following: GL_COLOR_INDEX, GL_RED, GL_GREEN, GL_BLUE, GL_ALPHA, GL_RGB, GL_RGBA, GL_BGR_EXT, GL_BGRA_EXT, GL_LUMINANCE, or GL_LUMINANCE_ALPHA.


### -param type

The data type for <i>data</i>. Must be one of the following: GL_UNSIGNED_BYTE, GL_BYTE, GL_BITMAP, GL_UNSIGNED_SHORT, GL_SHORT, GL_UNSIGNED_INT, GL_INT, or GL_FLOAT.


### -param data

A pointer to the image data in memory.


## -returns



This function does not return a value.




## -remarks



The <b>gluBuild2DMipmaps</b> function obtains the input image and generates all mipmap images (using <a href="https://msdn.microsoft.com/f47191e8-b22d-4f6a-949a-9c7782d6d338">gluScaleImage</a>) so the input image can be used as a mipmapped texture image. To load each of the images, call <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>. If the dimensions of the input image are not powers of two, then the image is scaled so that both the width and height are powers of two before the mipmaps are generated.

A return value of zero indicates success. Otherwise, a GLU error code is returned (see <a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a>).

For a description of the acceptable values for the <i>format</i> parameter, see <b>glTexImage2D</b>. For a description of the acceptable values for <i>type</i>, see <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/52ed924f-7a72-4458-b1b8-8e5d3021f60a">gluBuild1DMipmaps</a>



<a href="https://msdn.microsoft.com/f47191e8-b22d-4f6a-949a-9c7782d6d338">gluScaleImage</a>
 

 

