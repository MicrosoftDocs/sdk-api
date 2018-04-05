---
UID: NF:gl.glVertex2s
title: glVertex2s function
author: windows-driver-content
description: Specifies a vertex.
old-location: opengl\glvertex2s.htm
old-project: OpenGL
ms.assetid: e964d7b0-1cb7-4334-8861-1cc2ee37a71a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glVertex2s, glVertex2s, glVertex2s function [OpenGL], opengl.glvertex2s
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
-	Opengl32.dll
api_name:
-	glVertex2s
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glVertex2s function


## -description


Specifies a vertex.


## -parameters




### -param x

Specifies the x-coordinate of a vertex.


### -param y

Specifies the y-coordinate of a vertex.


## -returns



This function does not return a value.




## -remarks



The glVertex function commands are used within <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>/<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a> pairs to specify point, line, and polygon vertices. The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.

When only <i>x</i> and <i>y</i> are specified, <i>z</i> defaults to 0.0 and <i>w</i> defaults to 1.0. When <i>x</i>, <i>y</i>, and <i>z</i> are specified, <i>w</i> defaults to 1.0.

Invoking glVertex outside of a <b>glBegin</b>/<b>glEnd</b> pair results in undefined behavior.





## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>



<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>



<a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>



<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>



<a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>



<a href="https://msdn.microsoft.com/f68ab938-49f8-42ea-afa7-691227b6f877">glRect</a>



<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>
 

 

