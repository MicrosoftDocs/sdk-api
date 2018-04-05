---
UID: NF:gl.glGetPointerv
title: glGetPointerv function
author: windows-driver-content
description: The glGetPointerv function returns the address of a vertex data array.
old-location: opengl\glgetpointerv.htm
old-project: OpenGL
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glGetPointerv, gl/glGetPointerv, glGetPointerv, glGetPointerv function [OpenGL], opengl.glgetpointerv"
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
-	glGetPointerv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetPointerv function


## -description


The <b>glGetPointerv</b> function returns the address of a vertex data array.


## -parameters




### -param pname

The type of array pointer to return from the following symbolic constants: GL_COLOR_ARRAY_POINTER, GL_EDGE_FLAG_ARRAY_POINTER, GL_FEEDBACK_BUFFER_POINTER, GL_INDEX_ARRAY_POINTER, GL_NORMAL_ARRAY_POINTER, GL_TEXTURE_COORD_ARRAY_POINTER, GL_SELECTION_BUFFER_POINTER, and GL_VERTEX_ARRAY_POINTER.


### -param params

Returns the value of the array pointer specified by <i>pname</i>.


## -returns



This function does not return a value.




## -remarks



The <b>glGetPointerv</b> function returns array pointer information. The <i>pname</i> parameter is a symbolic constant specifying the kind of array pointer to return, and <i>params</i> is a pointer to a location to place the returned data.




## -see-also




<a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>



<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/768e6ec2-3f00-44e6-b3cb-de0f06d6a73d">glGetString</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

