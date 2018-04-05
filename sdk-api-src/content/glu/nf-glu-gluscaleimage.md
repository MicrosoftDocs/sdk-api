---
UID: NF:glu.gluScaleImage
title: gluScaleImage function
author: windows-driver-content
description: The gluScaleImage function scales an image to an arbitrary size.
old-location: opengl\gluscaleimage.htm
old-project: OpenGL
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluScaleImage, glu/gluScaleImage, gluScaleImage, gluScaleImage function [OpenGL], opengl.gluscaleimage"
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
-	gluScaleImage
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluScaleImage function


## -description


The <b>gluScaleImage</b> function scales an image to an arbitrary size.


## -parameters




### -param format

The format of the pixel data. The following symbolic values are valid: GL_COLOR_INDEX, GL_STENCIL_INDEX, GL_DEPTH_COMPONENT, GL_RED, GL_GREEN, GL_BLUE, GL_ALPHA, GL_RGB, GL_RGBA, GL_BGR_EXT, GL_BGRA_EXT, GL_LUMINANCE, and GL_LUMINANCE_ALPHA.


### -param widthin

The width of the source image that is scaled.


### -param heightin

The height of the source image that is scaled.


### -param typein

The data type for <i>datain</i>. Must be one of the following: GL_UNSIGNED_BYTE, GL_BYTE, GL_BITMAP, GL_UNSIGNED_SHORT, GL_SHORT, GL_UNSIGNED_INT, GL_INT, or GL_FLOAT.


### -param datain

A pointer to the source image.


### -param widthout

The width of the destination image.


### -param heightout

The height of the destination image.


### -param typeout

The data type for <i>dataout</i>. Must be one of the following: GL_UNSIGNED_BYTE, GL_BYTE, GL_BITMAP, GL_UNSIGNED_SHORT, GL_SHORT, GL_UNSIGNED_INT, GL_INT, or GL_FLOAT.


### -param dataout

A pointer to the destination image.


## -returns



If the function succeeds, the return value is zero.

If the function fails, the return value is a GLU error code (see <a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a>).




## -remarks



The <b>gluScaleImage</b> function scales a pixel image using the appropriate pixel store modes to unpack data from the source image and pack data into the destination image.

When shrinking an image, <b>gluScaleImage</b> uses a box filter to sample the source image and create pixels for the destination image. When magnifying an image, the pixels from the source image are linearly interpolated to create the destination image.

For a description of the acceptable values for the <i>format</i>, <i>typein</i>, and <i>typeout</i> parameters, see <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>



<a href="https://msdn.microsoft.com/52ed924f-7a72-4458-b1b8-8e5d3021f60a">gluBuild1DMipmaps</a>



<a href="https://msdn.microsoft.com/ea19a9b0-baf7-436f-afd5-609bc364b3ba">gluBuild2DMipmaps</a>



<a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a>
 

 

