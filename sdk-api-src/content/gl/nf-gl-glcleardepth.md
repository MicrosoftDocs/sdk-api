---
UID: NF:gl.glClearDepth
title: glClearDepth function
author: windows-driver-content
description: The glClearDepth function specifies the clear value for the depth buffer.
old-location: opengl\glcleardepth.htm
old-project: OpenGL
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glClearDepth, gl/glClearDepth, glClearDepth, glClearDepth function [OpenGL], opengl.glcleardepth"
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
-	glClearDepth
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glClearDepth function


## -description


The <b>glClearDepth</b> function specifies the clear value for the depth buffer.


## -parameters




### -param depth

The depth value used when the depth buffer is cleared.


## -returns



This function does not return a value.




## -remarks



The <b>glClearDepth</b> function specifies the depth value used by <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> to clear the depth buffer. Values specified by <b>glClearDepth</b> are clamped to the range [0,1].

The following function retrieves information related to the <b>glClearDepth</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_DEPTH_CLEAR_VALUE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
 

 

