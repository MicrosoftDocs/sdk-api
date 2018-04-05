---
UID: NF:gl.glTexCoordPointer
title: glTexCoordPointer function
author: windows-driver-content
description: The glTexCoordPointer function defines an array of texture coordinates.
old-location: opengl\gltexcoordpointer.htm
old-project: OpenGL
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glTexCoordPointer, gl/glTexCoordPointer, glTexCoordPointer, glTexCoordPointer function [OpenGL], opengl.gltexcoordpointer"
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
-	glTexCoordPointer
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glTexCoordPointer function


## -description


The <b>glTexCoordPointer</b> function defines an array of texture coordinates.


## -parameters




### -param size

The number of coordinates per array element. The value of <i>size</i> must be 1, 2, 3, or 4.


### -param type

The data type of each texture coordinate in the array using the following symbolic constants: <b>GL_SHORT</b>, <b>GL_INT</b>, <b>GL_FLOAT</b>, and <b>GL_DOUBLE</b>.


### -param stride

The byte offset between consecutive array elements. When <i>stride</i> is zero, the array elements are tightly packed in the array.


### -param pointer

A pointer to the first coordinate of the first element in the array.


## -returns



This function does not return a value.




## -remarks



The <b>glTexCoordPointer</b> function specifies the location and data of an array of texture coordinates to use when rendering.The <i>size</i> parameter specifies the number of coordinates used for each element of the array.The <i>type</i> parameter specifies the data type of each texture coordinate. The <i>stride</i> parameter determines the byte offset from one array element to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays. In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays. For more information, see <a href="https://msdn.microsoft.com/f1133949-d755-43e3-bf29-8e4c7fb17980">glInterleavedArrays</a>. When a texture coordinate array is specified, size, type, stride, and pointer are saved client-side state.

A texture coordinate array is enabled when you specify the <b>GL_TEXTURE_COORD_ARRAY</b> constant with <a href="https://msdn.microsoft.com/02520f81-0b0d-4774-b1e2-713cf226347f">glEnableClientState</a>. When enabled, <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>, and <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a> use the texture coordinate array. By default the texture coordinate array is disabled.

You cannot include <b>glTexCoordPointer</b> in display lists.

When you specify a texture coordinate array using <b>glTexCoordPointer</b>, the values of all the function's texture coordinate array parameters are saved in a client-side state, and static array elements can be cached. Because the texture coordinate array parameters are client-side state, their values are not saved or restored by <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> and <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>.

Although no error is generated when you call <b>glTexCoordPointer</b> within <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a> pairs, the results are undefined.

The following functions retrieve information related to <b>glTexCoordPointer</b>:


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument <b>GL_TEXTURE_COORD_ARRAY</b>


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument <b>GL_TEXTURE_COORD_ARRAY_SIZE</b>

<b>glGet</b> with argument <b>GL_TEXTURE_COORD_ARRAY_STRIDE</b>

<b>glGet</b> with argument <b>GL_TEXTURE_COORD_ARRAY_COUNT</b>

<b>glGet</b> with argument <b>GL_TEXTURE_COORD_ARRAY_TYPE</b>


<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a> with argument <b>GL_TEXTURE_COORD_ARRAY_POINTER</b>




## -see-also




<a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>



<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>



<a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a>



<a href="https://msdn.microsoft.com/768e6ec2-3f00-44e6-b3cb-de0f06d6a73d">glGetString</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/030a3955-35bf-4862-9691-54b0c24514e8">glPopClientAttrib</a>



<a href="https://msdn.microsoft.com/69f28af6-1023-4546-95ff-169525c23b07">glPushClientAttrib</a>



<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

