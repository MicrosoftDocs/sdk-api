---
UID: NF:gl.glGetClipPlane
title: glGetClipPlane function
author: windows-driver-content
description: The glGetClipPlane function returns the coefficients of the specified clipping plane.
old-location: opengl\glgetclipplane.htm
old-project: OpenGL
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glGetClipPlane, gl/glGetClipPlane, glGetClipPlane, glGetClipPlane function [OpenGL], opengl.glgetclipplane"
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
-	glGetClipPlane
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetClipPlane function


## -description


The <b>glGetClipPlane</b> function returns the coefficients of the specified clipping plane.


## -parameters




### -param plane

A clipping plane. The number of clipping planes depends on the implementation, but at least six clipping planes are supported. They are identified by symbolic names of the form GL_CLIP_PLANE <i>i</i> where 0 ≤ <i>i</i> &lt; GL_MAX_CLIP_PLANES.


### -param equation

Returns four double-precision values that are the coefficients of the plane equation of <i>plane</i> in eye coordinates.


## -returns



This function does not return a value.




## -remarks



The <b>glGetClipPlane</b> function returns in <i>equation</i> the four coefficients of the plane equation for <i>plane</i>.

It is always the case that GL_CLIP_PLANE<i>i</i> = GL_CLIP_PLANE0 + <i>i</i>.

If an error is generated, no change is made to the contents of <i>equation</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/b70d2c30-7502-4399-8c08-5ec9a2a1919c">glClipPlane</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>
 

 

