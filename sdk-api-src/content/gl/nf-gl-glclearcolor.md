---
UID: NF:gl.glClearColor
title: glClearColor function
author: windows-driver-content
description: The glClearColor function specifies clear values for the color buffers.
old-location: opengl\glclearcolor.htm
old-project: OpenGL
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glClearColor, gl/glClearColor, glClearColor, glClearColor function [OpenGL], opengl.glclearcolor"
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
-	glClearColor
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glClearColor function


## -description


The <b>glClearColor</b> function specifies clear values for the color buffers.


## -parameters




### -param red

The red value that <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> uses to clear the color buffers. The default value is zero. 



### -param green

The green value that <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> uses to clear the color buffers. The default value is zero. 



### -param blue

The blue value that <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> uses to clear the color buffers. The default value is zero. 



### -param alpha

The alpha value that <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> uses to clear the color buffers. The default value is zero. 



## -returns



This function does not return a value.




## -remarks



The <b>glClearColor</b> function specifies the red, green, blue, and alpha values used by <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> to clear the color buffers. Values specified by <b>glClearColor</b> are clamped to the range [0,1].

The following functions retrieve information related to the <b>glClearColor</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_ACCUM_CLEAR_VALUE

<b>glGet</b> with argument GL_COLOR_CLEAR_VALUE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
 

 

