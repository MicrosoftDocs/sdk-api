---
UID: NF:gl.glNormalPointer
title: glNormalPointer function
author: windows-driver-content
description: The glNormalPointer function defines an array of normals.
old-location: opengl\glnormalpointer.htm
old-project: OpenGL
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glNormalPointer, gl/glNormalPointer, glNormalPointer, glNormalPointer function [OpenGL], opengl.glnormalpointer"
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
-	glNormalPointer
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glNormalPointer function


## -description


The <b>glNormalPointer</b> function defines an array of normals.


## -parameters




### -param type

The data type of each coordinate in the array using the following symbolic constants: GL_BYTE, GL_SHORT, GL_INT, GL_FLOAT, and GL_DOUBLE.


### -param stride

The byte offset between consecutive normals. When <i>stride</i> is zero, the normals are tightly packed in the array.


### -param pointer

A pointer to the first normal in the array.


## -returns



This function does not return a value.




## -remarks



The <b>glNormalPointer</b> function specifies the location and data of an array of normals to use when rendering. The <i>type</i> parameter specifies the data type of each normal coordinate. The <i>stride</i> parameter determines the byte offset from one normal to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays. In some implementations storing the vertices and attributes in a single array can be more efficient than using separate arrays; see <a href="https://msdn.microsoft.com/f1133949-d755-43e3-bf29-8e4c7fb17980">glInterleavedArrays</a> for details.

A normal array is enabled when you specify the GL_NORMAL_ARRAY constant with <a href="https://msdn.microsoft.com/02520f81-0b0d-4774-b1e2-713cf226347f">glEnableClientState</a>. When enabled, <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a> and <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a> use the normal array. By default the normal array is disabled.

You cannot include <b>glNormalPointer</b> in display lists.

When you specify a normal array using <b>glNormalPointer</b>, the values of all the function's normal array parameters are saved in a client-side state. Because the normal array parameters are saved in a client-side state, their values are not saved or restored by <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> and <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>.

Although no error is generated when you call <b>glNormalPointer</b> within <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a> pairs, the results are undefined.

The following functions are associated with <b>glNormalPointer</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_NORMAL_ARRAY_STRIDE

<b>glGet</b> with argument GL_NORMAL_ARRAY_COUNT

<b>glGet</b> with argument GL_NORMAL_ARRAY_TYPE

<b>glGetPointerv</b> with argument GL_NORMAL_ARRAY_POINTER


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_NORMAL_ARRAY




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



<a href="https://msdn.microsoft.com/f1133949-d755-43e3-bf29-8e4c7fb17980">glInterleavedArrays</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

