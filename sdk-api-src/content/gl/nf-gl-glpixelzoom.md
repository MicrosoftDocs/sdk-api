---
UID: NF:gl.glPixelZoom
title: glPixelZoom function
author: windows-driver-content
description: The glPixelZoom function specifies the pixel zoom factors.
old-location: opengl\glpixelzoom.htm
old-project: OpenGL
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glPixelZoom, gl/glPixelZoom, glPixelZoom, glPixelZoom function [OpenGL], opengl.glpixelzoom"
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
-	glPixelZoom
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPixelZoom function


## -description


The <b>glPixelZoom</b> function specifies the pixel zoom factors.


## -parameters




### -param xfactor

The <i>x</i> zoom factor for pixel write operations.


### -param yfactor

The <i>y</i> zoom factor for pixel write operations.


## -returns



This function does not return a value.




## -remarks



The <b>glPixelZoom</b> function specifies values for the <i>x</i> and <i>y</i> zoom factors. During the execution of <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a> or <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>, if (<i>x</i><sub>r</sub> ,<i>y</i><sub>r</sub> ) is the current raster position, and a given element is in the <i>n</i>th row and <i>m</i>th column of the pixel rectangle, then pixels whose centers are in the rectangle with corners at

<img alt="" border="0" src="images/pix05.png"/>
are candidates for replacement. Any pixel whose center lies on the bottom or left edge of this rectangular region is also modified.

Pixel zoom factors are not limited to positive values. Negative zoom factors reflect the resulting image about the current raster position.

The following functions retrieve information related to <b>glPixelZoom</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_ZOOM_X

<b>glGet</b> with argument GL_ZOOM_Y




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>
 

 

