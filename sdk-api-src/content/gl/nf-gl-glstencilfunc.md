---
UID: NF:gl.glStencilFunc
title: glStencilFunc function
author: windows-driver-content
description: The glStencilFunc function sets the function and reference value for stencil testing.
old-location: opengl\glstencilfunc.htm
old-project: OpenGL
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ALWAYS, GL_EQUAL, GL_GEQUAL, GL_GREATER, GL_LEQUAL, GL_LESS, GL_NEVER, GL_NOTEQUAL, _ogl_glStencilFunc, gl/glStencilFunc, glStencilFunc, glStencilFunc function [OpenGL], opengl.glstencilfunc
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
-	glStencilFunc
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glStencilFunc function


## -description


The <b>glStencilFunc</b> function sets the function and reference value for stencil testing.


## -parameters




### -param func

The test function. The following eight tokens are valid.

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
Always fails.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LESS"></a><a id="gl_less"></a><dl>
<dt><b>GL_LESS</b></dt>
</dl>
</td>
<td width="60%">
Passes if (<i>ref</i> &amp; <i>mask</i>) &lt; (<i>stencil</i> &amp; <i>mask</i>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LEQUAL"></a><a id="gl_lequal"></a><dl>
<dt><b>GL_LEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if (<i>ref</i> &amp; <i>mask</i>) ≤ (<i>stencil</i> &amp; <i>mask</i>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GREATER"></a><a id="gl_greater"></a><dl>
<dt><b>GL_GREATER</b></dt>
</dl>
</td>
<td width="60%">
Passes if (<i>ref</i> &amp; <i>mask</i>) &gt; (<i>stencil</i> &amp; <i>mask</i>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GEQUAL"></a><a id="gl_gequal"></a><dl>
<dt><b>GL_GEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if (<i>ref</i> &amp; <i>mask</i>) ≥ (<i>stencil</i> &amp; <i>mask</i>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EQUAL"></a><a id="gl_equal"></a><dl>
<dt><b>GL_EQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if (<i>ref</i> &amp; <i>mask</i>) = (<i>stencil</i> &amp; <i>mask</i>).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NOTEQUAL"></a><a id="gl_notequal"></a><dl>
<dt><b>GL_NOTEQUAL</b></dt>
</dl>
</td>
<td width="60%">
Passes if (<i>ref</i> &amp; <i>mask</i>) ≠ (<i>stencil</i> &amp; <i>mask</i>).

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
 


### -param ref

The reference value for the stencil test. The <i>ref</i> parameter is clamped to the range [0, 2<i>ⁿ</i> 1], where <i>n</i> is the number of bitplanes in the stencil buffer.


### -param mask

A mask that is <b>AND</b>ed with both the reference value and the stored stencil value when the test is done.


## -returns



This function does not return a value.




## -remarks



Stenciling, like <i>z</i>-buffering, enables and disables drawing on a per-pixel basis. You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen. Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.

The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the reference value and the value in the stencil buffer. The test is enabled by <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a> with argument GL_STENCIL_TEST. Actions taken based on the outcome of the stencil test are specified with <a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>.

The <i>func</i> parameter is a symbolic constant that determines the stencil comparison function. It accepts one of the eight values shown above. The <i>ref</i> parameter is an integer reference value that is used in the stencil comparison. It is clamped to the range [0, 2<i>ⁿ</i> 1], where <i>n</i> is the number of bitplanes in the stencil buffer. The <i>mask</i> parameter is bitwise <b>AND</b>ed with both the reference value and the stored stencil value, with the <b>AND</b>ed values participating in the comparison.

If <i>stencil</i> represents the value stored in the corresponding stencil buffer location, the preceding list shows the effect of each comparison function that can be specified by <i>func</i>. Only if the comparison succeeds is the pixel passed through to the next stage in the rasterization process (see <a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>). All tests treat <i>stencil</i> values as unsigned integers in the range [0, 2<i>ⁿ</i> 1], where <i>n</i> is the number of bitplanes in the stencil buffer.

Initially, the stencil test is disabled. If there is no stencil buffer, no stencil modification can occur and it is as if the stencil test always passes.

The following functions retrieve information related to <b>glStencilFunc</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_STENCIL_FUNC

<b>glGet</b> with argument GL_STENCIL_VALUE_MASK

<b>glGet</b> with argument GL_STENCIL_REF

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



<a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>
 

 

