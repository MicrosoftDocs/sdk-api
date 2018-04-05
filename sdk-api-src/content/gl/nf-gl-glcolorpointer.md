---
UID: NF:gl.glColorPointer
title: glColorPointer function
author: windows-driver-content
description: The glColorPointer function defines an array of colors.
old-location: opengl\glcolorpointer.htm
old-project: OpenGL
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glColorPointer, gl/glColorPointer, glColorPointer, glColorPointer function [OpenGL], opengl.glcolorpointer"
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
-	glColorPointer
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glColorPointer function


## -description


The <b>glColorPointer</b> function defines an array of colors.


## -parameters




### -param size

The number of components per color. The value must be either 3 or 4.


### -param type

The data type of each color component in a color array. Acceptable data types are specified with the following constants: GL_BYTE, GL_UNSIGNED_BYTE, GL_SHORT, GL_UNSIGNED_SHORT, GL_INT, GL_UNSIGNED_INT, GL_FLOAT, or GL_DOUBLE.


### -param stride

The byte offset between consecutive colors. When <i>stride</i> is zero, the colors are tightly packed in the array.


### -param pointer

A pointer to the first component of the first color element in a color array.


## -returns



This function does not return a value.




## -remarks



The <b>glColorPointer</b> function specifies the location and data format of an array of color components to use when rendering. The <i>stride</i> parameter determines the byte offset from one color to the next, enabling the packing of vertex attributes in a single array or storage in separate arrays. In some implementations, storing vertex attributes in a single array can be more efficient than the use of separate arrays.

Enabled the color array by specifying the GL_COLOR_ARRAY constant with <a href="https://msdn.microsoft.com/02520f81-0b0d-4774-b1e2-713cf226347f">glEnableClientState</a>. Calling <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>, or <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a> uses the color array that is thus enabled. By default, the color array is disabled. The <b>glColorPointer</b> calls cannot by entered in display lists.

When you specify a color array using <b>glColorPointer</b>, the values of all the function's color array parameters are saved in a client-side state, and you can cache static array elements. Because the color array parameters are in a client-side state, <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> and <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a> do not save or restore the parameters' values.

Although specifying the color array within <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glend</a> pairs does not generate an error, the results are undefined.

The following functions retrieve information related to the <b>glColorPointer</b> function:


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_COLOR_ARRAY


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_COLOR_ARRAY_SIZE

<b>glGet</b> with argument GL_COLOR_ARRAY_TYPE

<b>glGet</b> with argument GL_COLOR_ARRAY_STRIDE

<b>glGet</b> with argument GL_COLOR_ARRAY_COUNT


<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a> with argument GL_COLOR_ARRAY_POINTER




## -see-also




<a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/02520f81-0b0d-4774-b1e2-713cf226347f">glEnableClientState</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a>



<a href="https://msdn.microsoft.com/768e6ec2-3f00-44e6-b3cb-de0f06d6a73d">glGetString</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>



<a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

