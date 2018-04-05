---
UID: NF:gl.glPolygonStipple
title: glPolygonStipple function
author: windows-driver-content
description: The glPolygonStipple function sets the polygon stippling pattern.
old-location: opengl\glpolygonstipple.htm
old-project: OpenGL
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glPolygonStipple, gl/glPolygonStipple, glPolygonStipple, glPolygonStipple function [OpenGL], opengl.glpolygonstipple"
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
-	glPolygonStipple
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPolygonStipple function


## -description


The <b>glPolygonStipple</b> function sets the polygon stippling pattern.


## -parameters




### -param mask

A pointer to a 32x32 stipple pattern that will be unpacked from memory in the same way that <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a> unpacks pixels.


## -returns



This function does not return a value.




## -remarks



The <b>glPolygonStipple</b> function sets the polygon stippling pattern. Polygon stippling, like line stippling (see <a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>), masks out certain fragments produced by rasterization, creating a pattern. Stippling is independent of polygon antialiasing.

The <i>mask</i> parameter is a pointer to a 32x32 stipple pattern that is stored in memory just like the pixel data supplied to <b>glDrawPixels</b> with <i>height</i> and <i>width</i> both equal to 32, a pixel <i>format</i> of GL_COLOR_INDEX, and data <i>type</i> of GL_BITMAP. That is, the stipple pattern is represented as a 32x32 array of 1-bit color indexes packed in unsigned bytes. The <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a> function parameters, such as GL_UNPACK_SWAP_BYTES and GL_UNPACK_LSB_FIRST, affect the assembling of the bits into a stipple pattern. Pixel transfer operations (shift, offset, and pixel map) are not applied to the stipple image, however.

Polygon stippling is enabled and disabled with <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b>, using argument GL_POLYGON_STIPPLE. If enabled, a rasterized polygon fragment with window coordinates <i>x</i><sub>w</sub> and <i>y</i><sub>w</sub> is sent to the next stage of OpenGL if and only if the (<i>x</i><sub>w</sub> mod 32)th bit in the (<i>y</i><sub>w</sub> mod 32)th row of the stipple pattern is one. When polygon stippling is disabled, it is as if the stipple pattern were all ones.

The following functions retrieve information related to <b>glPolygonStipple</b>:


<a href="https://msdn.microsoft.com/95c1ebfa-8465-4bc1-b3f5-eed696a83816">glGetPolygonStipple</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_POLYGON_STIPPLE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>
 

 

