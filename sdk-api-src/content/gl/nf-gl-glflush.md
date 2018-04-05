---
UID: NF:gl.glFlush
title: glFlush function
author: windows-driver-content
description: The glFlush function forces execution of OpenGL functions in finite time.
old-location: opengl\glflush.htm
old-project: OpenGL
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glFlush, gl/glFlush, glFlush, glFlush function [OpenGL], opengl.glflush"
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
-	glFlush
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glFlush function


## -description


The <b>glFlush</b> function forces execution of OpenGL functions in finite time.


## -parameters






## -returns



This function does not return a value.




## -remarks



Different OpenGL implementations buffer commands in several different locations, including network buffers and the graphics accelerator itself. The <b>glFlush</b> function empties all these buffers, causing all issued commands to be executed as quickly as they are accepted by the actual rendering engine. Though this execution may not be completed in any particular time period, it does complete in a finite amount of time.

Because any OpenGL program might be executed over a network, or on an accelerator that buffers commands, be sure to call <b>glFlush</b> in any programs requiring that all of their previously issued commands have been completed. For example, call <b>glFlush</b> before waiting for user input that depends on the generated image.

The <b>glFlush</b> function can return at any time. It does not wait until the execution of all previously issued OpenGL functions is complete.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/1dcb4767-02ea-41d8-bf1f-d61d20873d4f">glFinish</a>
 

 

