---
UID: NF:gl.glSelectBuffer
title: glSelectBuffer function
author: windows-driver-content
description: The glSelectBuffer function establishes a buffer for selection mode values.
old-location: opengl\glselectbuffer.htm
old-project: OpenGL
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glSelectBuffer, gl/glSelectBuffer, glSelectBuffer, glSelectBuffer function [OpenGL], opengl.glselectbuffer"
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
-	glSelectBuffer
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glSelectBuffer function


## -description


The <b>glSelectBuffer</b> function establishes a buffer for selection mode values.


## -parameters




### -param size

The size of <i>buffer</i>.


### -param buffer

Returns the selection data.


## -returns



This function does not return a value.




## -remarks



The <b>glSelectBuffer</b> function has two parameters: <i>buffer</i> is a pointer to an array of unsigned integers, and <i>size</i> indicates the size of the array. The <i>buffer</i> parameter returns values from the name stack (see <a href="https://msdn.microsoft.com/26c134f5-c17c-4637-93b6-5293f316dd6c">glInitNames</a>, <a href="https://msdn.microsoft.com/8d7d582b-3743-401e-af71-28034e49f3c2">glLoadName</a>, <a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a>) when the rendering mode is GL_SELECT (see <a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>). The <b>glSelectBuffer</b> function must be issued before selection mode is enabled, and it must not be issued while the rendering mode is GL_SELECT.

Selection is used by a programmer to determine which primitives are drawn into some region of a window. The region is defined by the current modelview and perspective matrices.

In selection mode, no pixel fragments are produced from rasterization. Instead, if a primitive intersects the clip volume defined by the viewing frustum and the user-defined clipping planes, this primitive causes a selection hit. (With polygons, no hit occurs if the polygon is culled.) When a change is made to the name stack, or when <a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a> is called, a hit record is copied to <i>buffer</i> if any hits have occurred since the last such event (either a name stack change or a <b>glRenderMode</b> call). The hit record consists of the number of names in the name stack at the time of the event; followed by the minimum and maximum depth values of all vertices that hit since the previous event; followed by the name stack contents, bottom name first.

Returned depth values are mapped such that the largest unsigned integer value corresponds to window coordinate depth 1.0, and zero corresponds to window coordinate depth 0.0.

An internal index into <i>buffer</i> is reset to zero whenever selection mode is entered. Each time a hit record is copied into <i>buffer</i>, the index is incremented to point to the cell just past the end of the block of namesthat is, to the next available cell. If the hit record is larger than the number of remaining locations in <i>buffer</i>, as much data as can fit is copied, and the overflow flag is set. If the name stack is empty when a hit record is copied, that record consists of zero followed by the minimum and maximum depth values.

Selection mode is exited by calling <b>glRenderMode</b> with an argument other than GL_SELECT. Whenever <b>glRenderMode</b> is called while the render mode is GL_SELECT, it returns the number of hit records copied to <i>buffer</i>, resets the overflow flag and the selection buffer pointer, and initializes the name stack to be empty. If the overflow bit was set when <b>glRenderMode</b> was called, a negative hit record count is returned.

The contents of <i>buffer</i> are undefined until <a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a> is called with an argument other than GL_SELECT.

The <b>glBegin</b>/<b>glEnd</b> primitives and calls to <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a> can result in hits.

The following function retrieves information related to <b>glSelectBuffer</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_NAME_STACK_DEPTH




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/fe3773a7-c264-4d49-8f90-1f2319f9af4f">glFeedbackBuffer</a>



<a href="https://msdn.microsoft.com/26c134f5-c17c-4637-93b6-5293f316dd6c">glInitNames</a>



<a href="https://msdn.microsoft.com/8d7d582b-3743-401e-af71-28034e49f3c2">glLoadName</a>



<a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a>



<a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>
 

 

