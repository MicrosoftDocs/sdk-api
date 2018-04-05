---
UID: NF:gl.glGetString
title: glGetString function
author: windows-driver-content
description: The glGetString function returns a string describing the current OpenGL connection.
old-location: opengl\glgetstring.htm
old-project: OpenGL
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_EXTENSIONS, GL_RENDERER, GL_VENDOR, GL_VERSION, _ogl_glGetString, gl/glGetString, glGetString, glGetString function [OpenGL], opengl.glgetstring
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
-	glGetString
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetString function


## -description


The <b>glGetString</b> function returns a string describing the current OpenGL connection.


## -parameters




### -param name

One of the following symbolic constants.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_VENDOR"></a><a id="gl_vendor"></a><dl>
<dt><b>GL_VENDOR</b></dt>
</dl>
</td>
<td width="60%">
Returns the company responsible for this OpenGL implementation. This name does not change from release to release.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RENDERER"></a><a id="gl_renderer"></a><dl>
<dt><b>GL_RENDERER</b></dt>
</dl>
</td>
<td width="60%">
Returns the name of the renderer. This name is typically specific to a particular configuration of a hardware platform. It does not change from release to release.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_VERSION"></a><a id="gl_version"></a><dl>
<dt><b>GL_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Returns a version or release number.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EXTENSIONS"></a><a id="gl_extensions"></a><dl>
<dt><b>GL_EXTENSIONS</b></dt>
</dl>
</td>
<td width="60%">
Returns a space-separated list of supported extensions to OpenGL.

</td>
</tr>
</table>
 


## -remarks



The <b>glGetString</b> function returns a pointer to a static string describing some aspect of the current OpenGL connection.

Because OpenGL does not include queries for the performance characteristics of an implementation, it is expected that some applications will be written to recognize known platforms and will modify their OpenGL usage based on known performance characteristics of these platforms. The strings GL_VENDOR and GL_RENDERER together uniquely specify a platform, and will not change from release to release. They should be used as such by platform recognition algorithms.

The format and contents of the string that <b>glGetString</b> returns depend on the implementation, except that:

<ul>
<li>Extension names will not include space characters and will be separated by space characters in the GL_EXTENSIONS string.</li>
<li>The GL_VERSION string begins with a version number. The version number uses one of these forms:

<i>major_number</i>.<i>minor_number</i>

<i>major_number</i>.<i>minor_number</i>.<i>release_number</i>

</li>
<li>Vendor-specific information may follow the version number. Its format depends on the implementation, but a space always separates the version number and the vendor-specific information.</li>
<li>All strings are null-terminated.</li>
</ul>
If an error is generated, <b>glGetString</b> returns zero.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>
 

 

