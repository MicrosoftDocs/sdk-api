---
UID: NF:gl.glGetError
title: glGetError function
author: windows-driver-content
description: The glGetError function returns error information.
old-location: opengl\glgeterror.htm
old-project: OpenGL
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glGetError, gl/glGetError, glGetError, glGetError function [OpenGL], opengl.glgeterror"
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
-	glGetError
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetError function


## -description


The <b>glGetError</b> function returns error information.


## -parameters






## -returns



The <b>glGetError</b> function returns one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GL_INVALID_ENUM</b></dt>
</dl>
</td>
<td width="60%">
An unacceptable value is specified for an enumerated argument. The offending function is ignored, having no side effect other than to set the error flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GL_INVALID_VALUE</b></dt>
</dl>
</td>
<td width="60%">
A numeric argument is out of range. The offending function is ignored, having no side effect other than to set the error flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GL_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The specified operation is not allowed in the current state. The offending function is ignored, having no side effect other than to set the error flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GL_NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
No error has been recorded. The value of this symbolic constant is guaranteed to be zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GL_STACK_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
This function would cause a stack overflow. The offending function is ignored, having no side effect other than to set the error flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GL_STACK_UNDERFLOW</b></dt>
</dl>
</td>
<td width="60%">
This function would cause a stack underflow. The offending function is ignored, having no side effect other than to set the error flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GL_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory left to execute the function. The state of OpenGL is undefined, except for the state of the error flags, after this error is recorded.

</td>
</tr>
</table>
 

Note that <b>glGetError</b> returns GL_INVALID_OPERATION if it is called between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and its corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>.




## -remarks



Each detectable error is assigned a numeric code and symbolic name. When an error occurs, the error flag is set to the appropriate error code value. No other errors are recorded until <b>glGetError</b> is called, the error code is returned, and the flag is reset to GL_NO_ERROR. If a call to <b>glGetError</b> returns GL_NO_ERROR, there has been no detectable error since the last call to <b>glGetError</b>, or since OpenGL was initialized.

To allow for distributed implementations, there may be several error flags. If any single error flag has recorded an error, the value of that flag is returned and that flag is reset to GL_NO_ERROR when <b>glGetError</b> is called. If more than one flag has recorded an error, <b>glGetError</b> returns and clears an arbitrary error flag value. If all error flags are to be reset, you should always call <b>glGetError</b> in a loop until it returns GL_NO_ERROR.

Initially, all error flags are set to GL_NO_ERROR.

When an error flag is set, results of an OpenGL operation are undefined only if GL_OUT_OF_MEMORY has occurred. In all other cases, the function generating the error is ignored and has no effect on the OpenGL state or framebuffer contents.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>
 

 

