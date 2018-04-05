---
UID: NF:gl.glInterleavedArrays
title: glInterleavedArrays function
author: windows-driver-content
description: The glInterleavedArrays function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.
old-location: opengl\glinterleavedarrays.htm
old-project: OpenGL
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glInterleavedArrays, gl/glInterleavedArrays, glInterleavedArrays, glInterleavedArrays function [OpenGL], opengl.glinterleavedarrays"
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
-	glInterleavedArrays
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glInterleavedArrays function


## -description


The <b>glInterleavedArrays</b> function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.


## -parameters




### -param format

The type of array to enable. The parameter can assume one of the following symbolic values: GL_V2F, GL_V3F, GL_C4UB_V2F, GL_C4UB_V3F, GL_C3F_V3F, GL_N3F_V3F, GL_C4F_N3F_V3F, GL_T2F_V3F, GL_T4F_V4F, GL_T2F_C4UB_V3F, GL_T2F_C3F_V3F, GL_T2F_N3F_V3F, GL_T2F_C4F_N3F_V3F, or GL_T4F_C4F_N3F_V4F.


### -param stride

The offset in bytes between each aggregate array element.


### -param pointer

A pointer to the first element of an aggregate array.


## -returns



This function does not return a value.




## -remarks



With the <b>glInterleavedArrays</b> function, you can simultaneously specify and enable several interleaved color, normal, texture, and vertex arrays whose elements are part of a larger aggregate array element. For some memory architectures, this is more efficient than specifying the arrays separately.

If the <i>stride</i> parameter is zero then the aggregate array elements are stored consecutively; otherwise <i>stride</i> bytes occur between aggregate array elements.

The <i>format</i> parameter serves as a key that describes how to extract individual arrays from the aggregate array:

<ul>
<li>If <i>format</i> contains a T, then texture coordinates are extracted from the interleaved array.</li>
<li>If C is present, color values are extracted.</li>
<li>If N is present, normal coordinates are extracted.</li>
<li>Vertex coordinates are always extracted.</li>
<li>The digits 2, 3, and 4 denote how many values are extracted.</li>
<li>F indicates that values are extracted as floating point values.</li>
<li>If 4UB follows the C, colors may also be extracted as 4 unsigned bytes. If a color is extracted as 4 unsigned bytes, the vertex array element that follows is located at the first possible floating-point aligned address.</li>
</ul>
If you call <b>glInterleavedArrays</b> while compiling a display list, it is not compiled into the list but is executed immediately.

You cannot include calls to <b>glInterleavedArrays</b> in <b>glDisableClientState</b> between calls to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <b>glEnd</b>.

<div class="alert"><b>Note</b>  The <b>glInterleavedArrays</b> function is only available in OpenGL version 1.1 or later.</div>
<div> </div>
The <b>glInterleavedArrays</b> function is implemented on the client side with no protocol. Because the vertex array parameters are client-side state, they are not saved or restored by <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> and <b>glPopAttrib</b>. Use <a href="https://msdn.microsoft.com/69f28af6-1023-4546-95ff-169525c23b07">glPushClientAttrib</a> and <b>glPopClientAttrib</b> instead.




## -see-also




<a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>



<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>



<a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/02520f81-0b0d-4774-b1e2-713cf226347f">glEnableClientState</a>



<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>



<a href="https://msdn.microsoft.com/69f28af6-1023-4546-95ff-169525c23b07">glPushClientAttrib</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

