---
UID: NF:gl.glDrawElements
title: glDrawElements function
author: windows-driver-content
description: The glDrawElements function renders primitives from array data.
old-location: opengl\gldrawelements.htm
old-project: OpenGL
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glDrawElements, gl/glDrawElements, glDrawElements, glDrawElements function [OpenGL], opengl.gldrawelements"
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
-	glDrawElements
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glDrawElements function


## -description


The <b>glDrawElements</b> function renders primitives from array data.


## -parameters




### -param mode

The kind of primitives to render. It can assume one of the following symbolic values: GL_POINTS, GL_LINE_STRIP, GL_LINE_LOOP, GL_LINES, GL_TRIANGLE_STRIP, GL_TRIANGLE_FAN, GL_TRIANGLES, GL_QUAD_STRIP, GL_QUADS, and GL_POLYGON.


### -param count

The number of elements to be rendered.


### -param type

The type of the values in indices. Must be one of GL_UNSIGNED_BYTE, GL_UNSIGNED_SHORT, or GL_UNSIGNED_INT.


### -param indices

A pointer to the location where the indices are stored.


## -returns



This function does not return a value.




## -remarks



The <b>glDrawElements</b> function enables you to specify multiple geometric primitives with very few function calls. Instead of calling an OpenGL function to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors beforehand and use them to define a sequence of primitives (all of the same type) with a single call to <b>glDrawElements</b>.

When you call the <b>glDrawElements</b> function, it uses <i>count</i> sequential elements from <i>indices</i> to construct a sequence of geometric primitives. The <i>mode</i> parameter specifies what kind of primitives are constructed, and how the array elements are used to construct these primitives. If GL_VERTEX_ARRAY is not enabled, no geometric primitives are generated.

Vertex attributes that are modified by <b>glDrawElements</b> have an unspecified value after <b>glDrawElements</b> returns. For example, if GL_COLOR_ARRAY is enabled, the value of the current color is undefined after <b>glDrawElements</b> executes. Attributes that aren't modified remain unchanged.

You can include the <b>glDrawElements</b> function in display lists. When <b>glDrawElements</b> is included in a display list, the necessary array data (determined by the array pointers and enables) is also entered into the display list. Because the array pointers and enables are client-side state variables, their values affect display lists when the lists are created, not when the lists are executed.

<div class="alert"><b>Note</b>  The <b>glDrawElements</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

