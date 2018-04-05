---
UID: NF:gl.glColor3i
title: glColor3i function
author: windows-driver-content
description: Sets the current color.
old-location: opengl\glcolor3i.htm
old-project: OpenGL
ms.assetid: 9c68221b-1633-435b-9ae4-abc1c52601aa
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glColor3i, glColor3i, glColor3i function [OpenGL], opengl.glcolor3i
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
-	glColor3i
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glColor3i function


## -description


Sets the current color.


## -parameters




### -param red

The new red value for the current color.


### -param green

The new green value for the current color.


### -param blue

The new blue value for the current color.


## -returns



This function does not return a value.




## -remarks



The GL stores both a current single-valued color index and a current four-valued RGBA color. <b>glcolor</b> sets a new four-valued RGBA color. <b>glcolor</b> has two major variants: <b>glcolor3</b> and <b>glcolor4</b>. <b>glcolor3</b> variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly. <b>glcolor4</b> variants specify all four color components explicitly. 



<b>glcolor3b</b>, <b>glcolor4b</b>, <b>glcolor3s</b>, <b>glcolor4s</b>, <b>glcolor3i</b>, and <b>glcolor4i</b> take three or four signed byte, short, or long integers as arguments. When v is appended to the name, the color commands can take a pointer to an array of such values. 



Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes. Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity). Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0. (Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly. 



Neither floating-point nor signed integer values are clamped to the range [0,1] before the current color is updated. However, color components are clamped to this range before they are interpolated or written into a color buffer. 






## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv</a>



<a href="https://msdn.microsoft.com/4cd72d32-e796-4c94-94cb-591f1ee3b26e">glIndex</a>
 

 

