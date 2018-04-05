---
UID: NF:gl.glStencilOp
title: glStencilOp function
author: windows-driver-content
description: The glStencilOp function sets the stencil test actions.
old-location: opengl\glstencilop.htm
old-project: OpenGL
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_DECR, GL_INCR, GL_INVERT, GL_KEEP, GL_REPLACE, GL_ZERO, _ogl_glStencilOp, gl/glStencilOp, glStencilOp, glStencilOp function [OpenGL], opengl.glstencilop
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
-	glStencilOp
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glStencilOp function


## -description


The <b>glStencilOp</b> function sets the stencil test actions.


## -parameters




### -param fail

The action to take when the stencil test fails. The following six symbolic constants are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_KEEP"></a><a id="gl_keep"></a><dl>
<dt><b>GL_KEEP</b></dt>
</dl>
</td>
<td width="60%">
Keeps the current value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ZERO"></a><a id="gl_zero"></a><dl>
<dt><b>GL_ZERO</b></dt>
</dl>
</td>
<td width="60%">
Sets the stencil buffer value to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_REPLACE"></a><a id="gl_replace"></a><dl>
<dt><b>GL_REPLACE</b></dt>
</dl>
</td>
<td width="60%">
Sets the stencil buffer value to <i>ref</i>, as specified by <b>glStencilFunc</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INCR"></a><a id="gl_incr"></a><dl>
<dt><b>GL_INCR</b></dt>
</dl>
</td>
<td width="60%">
Increments the current stencil buffer value. Clamps to the maximum representable unsigned value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DECR"></a><a id="gl_decr"></a><dl>
<dt><b>GL_DECR</b></dt>
</dl>
</td>
<td width="60%">
Decrements the current stencil buffer value. Clamps to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INVERT"></a><a id="gl_invert"></a><dl>
<dt><b>GL_INVERT</b></dt>
</dl>
</td>
<td width="60%">
Bitwise inverts the current stencil buffer value.

</td>
</tr>
</table>
 


### -param zfail

Stencil action when the stencil test passes, but the depth test fails. Accepts the same symbolic constants as <i>fail.</i>


### -param zpass

Stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled. Accepts the same symbolic constants as <i>fail</i>.


## -returns



This function does not return a value.




## -remarks



Stenciling, like <i>z</i>-buffering, enables and disables drawing on a per-pixel basis. You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen. Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.

The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the value in the stencil buffer and a reference value. The test is enabled with <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> calls with argument GL_STENCIL_TEST, and controlled with <a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>.

The <b>glStencilOp</b> function takes three arguments that indicate what happens to the stored stencil value while stenciling is enabled. If the stencil test fails, no change is made to the pixel's color or depth buffers, and <i>fail</i> specifies what happens to the stencil buffer contents.

Stencil buffer values are treated as unsigned integers. When incremented and decremented, values are clamped to 0 and 2<i>ⁿ</i> 1, where <i>n</i> is the value returned by querying GL_STENCIL_BITS.

The other two arguments to <b>glStencilOp</b> specify stencil buffer actions should subsequent depth buffer tests succeed (<i>zpass</i>) or fail (<i>zfail</i>). (See <a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>.) They are specified using the same six symbolic constants as <i>fail</i>. Note that <i>zfail</i> is ignored when there is no depth buffer, or when the depth buffer is not enabled. In these cases, <i>fail</i> and <i>zpass</i> specify stencil action when the stencil test fails and passes, respectively.

Initially the stencil test is disabled. If there is no stencil buffer, no stencil modification can occur and it is as if the stencil tests always pass, regardless of any call to <b>glStencilOp</b>.

The following functions retrieve information related to <b>glStencilOp</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_STENCIL_FAIL

<b>glGet</b> with argument GL_STENCIL_PASS_DEPTH_PASS

<b>glGet</b> with argument GL_STENCIL_PASS_DEPTH_FAIL

<b>glGet</b> with argument GL_STENCIL_BITS


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_STENCIL_TEST




## -see-also




<a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>



<a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>



<a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>
 

 

