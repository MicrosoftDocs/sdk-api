---
UID: NF:gl.glArrayElement
title: glArrayElement function
author: windows-driver-content
description: The glArrayElement function specifies the array elements used to render a vertex.
old-location: opengl\glarrayelement.htm
old-project: OpenGL
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glArrayElement, gl/glArrayElement, glArrayElement, glArrayElement function [OpenGL], opengl.glarrayelement"
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
-	glArrayElement
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glArrayElement function


## -description


The <b>glArrayElement</b> function specifies the array elements used to render a vertex.


## -parameters




### -param i

TBD




#### - index

An index in the enabled arrays.


## -returns



This function does not return a value.




## -remarks



Use the <b>glArrayElement</b> function within <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a> pairs to specify vertex and attribute data for point, line, and polygon primitives. The <b>glArrayElement</b> function specifies the data for a single vertex using vertex and attribute data located at the <i>index</i> of the enabled vertex arrays.

You can use <b>glArrayElement</b> to construct primitives by indexing vertex data, rather than by streaming through arrays of data in first-to-last order. Because <b>glArrayElement</b> specifies a single vertex only, you can explicitly specify attributes for individual primitives. For example, you can set a single normal for each individual triangle.

When you include calls to <b>glArrayElement</b> in display lists, the necessary array data, determined by the array pointers and enable values, is entered in the display list also. Array pointer and enable values are determined when display lists are created, not when display lists are executed.

You can read and cache static array data at any time with <b>glArrayElement</b>. When you modify the elements of a static array without specifying the array again, the results of any subsequent calls to <b>glArrayElement</b> are undefined.

When you call <b>glArrayElement</b> without first calling <b>glEnableClientState</b>(GL_VERTEX_ARRAY), no drawing occurs, but the attributes corresponding to enabled arrays are modified. Although no error is generated when you specify an array within <b>glBegin</b> and <b>glEnd</b> pairs, the results are undefined.

<div class="alert"><b>Note</b>  The <b>glArrayElement</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/02520f81-0b0d-4774-b1e2-713cf226347f">glEnableClientState</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a>



<a href="https://msdn.microsoft.com/768e6ec2-3f00-44e6-b3cb-de0f06d6a73d">glGetString</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

