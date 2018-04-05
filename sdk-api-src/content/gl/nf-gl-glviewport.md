---
UID: NF:gl.glViewport
title: glViewport function
author: windows-driver-content
description: The glViewport function sets the viewport.
old-location: opengl\glviewport.htm
old-project: OpenGL
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glViewport, gl/glViewport, glViewport, glViewport function [OpenGL], opengl.glviewport"
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
-	glViewport
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glViewport function


## -description


The <b>glViewport</b> function sets the viewport.


## -parameters




### -param x

The lower-left corner of the viewport rectangle, in pixels. The default is (0,0).


### -param y

The lower-left corner of the viewport rectangle, in pixels. The default is (0,0).


### -param width

The width of the viewport. When an OpenGL context is first attached to a window, <i>width</i> and <i>height</i> are set to the dimensions of that window.


### -param height

The height of the viewport. When an OpenGL context is first attached to a window, <i>width</i> and <i>height</i> are set to the dimensions of that window.


## -returns



This function does not return a value.




## -remarks



The <b>glViewport</b> function specifies the affine transformation of <i>x</i> and <i>y</i> from normalized device coordinates to window coordinates. Let (<i>x</i><sub>nd</sub> , <i>y</i><sub>nd</sub> ) be normalized device coordinates. The window coordinates (<i>x</i><sub>w</sub> , <i>y</i><sub>w</sub> ) are then computed as follows:

<img alt="" border="0" src="images/view01.png"/>
Viewport width and height are silently clamped to a range that depends on the implementation. This range is queried by calling <b>glGet</b> with argument GL_MAX_VIEWPORT_DIMS.

The following functions retrieve information related to <b>glViewport</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_VIEWPORT

<b>glGet</b> with argument GL_MAX_VIEWPORT_DIMS




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>
 

 

