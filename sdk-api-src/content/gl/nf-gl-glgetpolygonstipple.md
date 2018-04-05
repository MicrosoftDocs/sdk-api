---
UID: NF:gl.glGetPolygonStipple
title: glGetPolygonStipple function
author: windows-driver-content
description: The glGetPolygonStipple function returns the polygon stipple pattern.
old-location: opengl\glgetpolygonstipple.htm
old-project: OpenGL
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glGetPolygonStipple, gl/glGetPolygonStipple, glGetPolygonStipple, glGetPolygonStipple function [OpenGL], opengl.glgetpolygonstipple"
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
-	glGetPolygonStipple
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetPolygonStipple function


## -description


The <b>glGetPolygonStipple</b> function returns the polygon stipple pattern.


## -parameters




### -param mask

Returns the stipple pattern.


## -returns



This function does not return a value.




## -remarks



The <b>glGetPolygonStipple</b> function returns a 32x32 polygon stipple pattern through the <i>mask</i> parameter. The pattern is packed into memory as if <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a> with both <i>height</i> and <i>width</i> of 32, <i>type</i> of GL_BITMAP, and <i>format</i> of GL_COLOR_INDEX were called, and the stipple pattern were stored in an internal 32x32 color-index buffer. Unlike <b>glReadPixels</b>, however, pixel-transfer operations (shift, offset, and pixel map) are not applied to the returned stipple image.

If an error is generated, no change is made to the contents of <i>mask</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>
 

 

