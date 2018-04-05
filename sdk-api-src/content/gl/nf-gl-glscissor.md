---
UID: NF:gl.glScissor
title: glScissor function
author: windows-driver-content
description: The glScissor function defines the scissor box.
old-location: opengl\glscissor.htm
old-project: OpenGL
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glScissor, gl/glScissor, glScissor, glScissor function [OpenGL], opengl.glscissor"
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
-	glScissor
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glScissor function


## -description


The <b>glScissor</b> function defines the scissor box.


## -parameters




### -param x

The x (vertical axis) coordinate for the lower-left corner of the scissor box.			     


### -param y

The y (horizontal axis) coordinate for the lower-left corner of the scissor box. Together, x and y specify the lower-left corner of the scissor box. Initially (0,0).


### -param width

The width of the scissor box.


### -param height

The height of the scissor box. When an OpenGL context is <i>first</i> attached to a window, <i>width</i> and <i>height</i> are set to the dimensions of that window.


## -returns



This function does not return a value.




## -remarks



The <b>glScissor</b> function defines a rectangle, called the scissor box, in window coordinates. The first two parameters, <i>x</i> and <i>y</i>, specify the lower-left corner of the box. The <i>width</i> and <i>height</i> parameters specify the width and height of the box.

The scissor test is enabled and disabled using <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> with argument GL_SCISSOR_TEST. While the scissor test is enabled, only pixels that lie within the scissor box can be modified by drawing commands. Window coordinates have integer values at the shared corners of framebuffer pixels, so <b>glScissor</b>(0,0,1,1) allows only the lower-left pixel in the window to be modified, and <b>glScissor</b>(0,0,0,0) disallows modification to all pixels in the window.

When the scissor test is disabled, it is as though the scissor box includes the entire window.

The following functions retrieve information related to <b>glScissor</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_SCISSOR_BOX


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_SCISSOR_TEST




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/11816b2f-ee18-42ef-a782-2e96699dd087">glViewport</a>
 

 

