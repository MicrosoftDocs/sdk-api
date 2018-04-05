---
UID: NF:gl.glDepthFunc
title: glDepthFunc function
author: windows-driver-content
description: The glDepthFunc function specifies the value used for depth-buffer comparisons.
old-location: opengl\gldepthfunc.htm
old-project: OpenGL
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ALWAYS, GL_EQUAL, GL_GEQUAL, GL_GREATER, GL_LEQUAL, GL_LESS, GL_NEVER, GL_NOTEQUAL, _ogl_glDepthFunc, gl/glDepthFunc, glDepthFunc, glDepthFunc function [OpenGL], opengl.gldepthfunc
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
-	glDepthFunc
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glDepthFunc function


## -description


The <b>glDepthFunc</b> function specifies the value used for depth-buffer comparisons.


## -parameters




### -param func

Specifies the depth-comparison function. The following symbolic constants are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_NEVER"></a><a id="gl_never"></a><dl>
<dt><b>GL_NEVER</b></dt>
</dl>
</td>
<td width="60%">
Never passes.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LESS"></a><a id="gl_less"></a><dl>
<dt><b>GL_LESS</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming <i>z</i> value is less than the stored <i>z</i> value. This is the default value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LEQUAL"></a><a id="gl_lequal"></a><dl>
<dt><b>GL_LEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming z value is less than or equal to the stored z value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EQUAL"></a><a id="gl_equal"></a><dl>
<dt><b>GL_EQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming z value is equal to the stored z value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GREATER"></a><a id="gl_greater"></a><dl>
<dt><b>GL_GREATER</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming z value is greater than the stored z value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NOTEQUAL"></a><a id="gl_notequal"></a><dl>
<dt><b>GL_NOTEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming z value is not equal to the stored z value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GEQUAL"></a><a id="gl_gequal"></a><dl>
<dt><b>GL_GEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if the incoming z value is greater than or equal to the stored z value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALWAYS"></a><a id="gl_always"></a><dl>
<dt><b>GL_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Always passes.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>glDepthFunc</b> function specifies the function used to compare each incoming pixel <i>z</i> value with the <i>z</i> value present in the depth buffer. The comparison is performed only if depth testing is enabled. (See <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> with the argument GL_DEPTH_TEST.)

Initially, depth testing is disabled.

The following functions retrieve information related to <b>glDepthFunc</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_DEPTH_FUNC


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_DEPTH_TEST




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>
 

 

