---
UID: NF:gl.glDrawArrays
title: glDrawArrays function
author: windows-driver-content
description: The glDrawArrays function specifies multiple primitives to render.
old-location: opengl\gldrawarrays.htm
old-project: OpenGL
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glDrawArrays, gl/glDrawArrays, glDrawArrays, glDrawArrays function [OpenGL], opengl.gldrawarrays"
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
-	glDrawArrays
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glDrawArrays function


## -description


The <b>glDrawArrays</b> function specifies multiple primitives to render.


## -parameters




### -param mode

The kind of primitives to render. The following constants specify acceptable types of primitives: GL_POINTS, GL_LINE_STRIP, GL_LINE_LOOP, GL_LINES, GL_TRIANGLE_STRIP, GL_TRIANGLE_FAN, GL_TRIANGLES, GL_QUAD_STRIP, GL_QUADS, and GL_POLYGON.


### -param first

The starting index in the enabled arrays.


### -param count

The number of indexes to render.


## -returns



This function does not return a value.




## -remarks



With <b>glDrawArrays</b>, you can specify multiple geometric primitives to render. Instead of calling separate OpenGL functions to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors to define a sequence of primitives (all the same kind) with a single call to <b>glDrawArrays</b>.

When you call <b>glDrawArrays</b>, <i>count</i> sequential elements from each enabled array are used to construct a sequence of geometric primitives, beginning with the <i>first</i> element. The <i>mode</i> parameter specifies what kind of primitive to construct and how to use the array elements to construct the primitives.

After <b>glDrawArrays</b> returns, the values of vertex attributes that are modified by <b>glDrawArrays</b> are undefined. For example, if GL_COLOR_ARRAY is enabled, the value of the current color is undefined after <b>glDrawArrays</b> returns. Attributes not modified by <b>glDrawArrays</b> remain defined. When GL_VERTEX_ARRAY is not enabled, no geometric primitives are generated but the attributes corresponding to enabled arrays are modified.

You can include <b>glDrawArrays</b> in display lists. When you include <b>glDrawArrays</b> in a display list, the necessary array data, determined by the array pointers and the enables, are generated and entered in the display list. The values of array pointers and enables are determined during the creation of display lists.

You can read static array data at any time. If any static array elements are modified and the array is not specified again, the results of any subsequent calls to <b>glDrawArrays</b> are undefined.

Although no error is generated when you specify an array more than once within <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glend</a> pairs, the results are undefined.




## -see-also




<a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a>



<a href="https://msdn.microsoft.com/768e6ec2-3f00-44e6-b3cb-de0f06d6a73d">glGetString</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

