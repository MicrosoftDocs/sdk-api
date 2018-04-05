---
UID: NF:gl.glFinish
title: glFinish function
author: windows-driver-content
description: The glFinish function blocks until all OpenGL execution is complete.
old-location: opengl\glfinish.htm
old-project: OpenGL
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glFinish, gl/glFinish, glFinish, glFinish function [OpenGL], opengl.glfinish"
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
-	glFinish
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glFinish function


## -description


The <b>glFinish</b> function blocks until all OpenGL execution is complete.


## -parameters






## -returns



This function does not return a value.




## -remarks



The <b>glFinish</b> function does not return until the effects of all previously called OpenGL functions are complete. Such effects include all changes to the OpenGL state, all changes to the connection state, and all changes to the framebuffer contents.

The <b>glFinish</b> function requires a round trip to the server.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7544b724-472f-4055-8f1c-64ddb58caaf3">glFlush</a>
 

 

