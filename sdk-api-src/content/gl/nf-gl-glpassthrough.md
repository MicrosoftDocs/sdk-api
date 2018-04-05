---
UID: NF:gl.glPassThrough
title: glPassThrough function
author: windows-driver-content
description: The glPassThrough function places a marker in the feedback buffer.
old-location: opengl\glpassthrough.htm
old-project: OpenGL
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_PASS_THROUGH_TOKEN, _ogl_glPassThrough, gl/glPassThrough, glPassThrough, glPassThrough function [OpenGL], opengl.glpassthrough
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
-	glPassThrough
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPassThrough function


## -description


The <b>glPassThrough</b> function places a marker in the feedback buffer.


## -parameters




### -param token

A marker value to be placed in the feedback buffer. It is indicated with the following unique identifying value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_PASS_THROUGH_TOKEN"></a><a id="gl_pass_through_token"></a><dl>
<dt><b>GL_PASS_THROUGH_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
The order of <b>glPassThrough</b> commands with respect to the specification of graphics primitives is maintained.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



Feedback is an OpenGL render mode selected by calling <a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a> with GL_FEEDBACK. When OpenGL is in feedback mode, no pixels are produced by rasterization. Instead, information about primitives that would have been rasterized is fed back to the application by OpenGL. See <a href="https://msdn.microsoft.com/fe3773a7-c264-4d49-8f90-1f2319f9af4f">glFeedbackBuffer</a> for a description of the feedback buffer and the values in it.

The <b>glPassThrough</b> function inserts a user-defined marker in the feedback buffer when it is executed in feedback mode. The <i>token</i> parameter is returned as if it were a primitive.

The <b>glPassThrough</b> function is ignored if OpenGL is not in feedback mode.

The following function retrieves information related to <b>glPassThrough</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_RENDER_MODE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/fe3773a7-c264-4d49-8f90-1f2319f9af4f">glFeedbackBuffer</a>



<a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>
 

 

