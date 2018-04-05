---
UID: NF:gl.glRenderMode
title: glRenderMode function
author: windows-driver-content
description: The glRenderMode function sets the rasterization mode.
old-location: opengl\glrendermode.htm
old-project: OpenGL
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_FEEDBACK, GL_RENDER, GL_SELECT, _ogl_glRenderMode, gl/glRenderMode, glRenderMode, glRenderMode function [OpenGL], opengl.glrendermode
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
-	glRenderMode
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glRenderMode function


## -description


The <b>glRenderMode</b> function sets the rasterization mode.


## -parameters




### -param mode

The rasterization mode. The following three values are accepted. The default value is GL_RENDER.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_RENDER"></a><a id="gl_render"></a><dl>
<dt><b>GL_RENDER</b></dt>
</dl>
</td>
<td width="60%">
Render mode. Primitives are rasterized, producing pixel fragments, which are written into the framebuffer. This is the normal mode and also the default mode.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SELECT"></a><a id="gl_select"></a><dl>
<dt><b>GL_SELECT</b></dt>
</dl>
</td>
<td width="60%">
Selection mode. No pixel fragments are produced, and no change to the framebuffer contents is made. Instead, a record of the names of primitives that would have been drawn if the render mode was GL_RENDER is returned in a select buffer, which must be created (see <a href="https://msdn.microsoft.com/b5c64364-1f47-4281-96b5-95c3f5c8e753">glSelectBuffer</a>) before selection mode is entered.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FEEDBACK"></a><a id="gl_feedback"></a><dl>
<dt><b>GL_FEEDBACK</b></dt>
</dl>
</td>
<td width="60%">
Feedback mode. No pixel fragments are produced, and no change to the framebuffer contents is made. Instead, the coordinates and attributes of vertices that would have been drawn had the render mode been GL_RENDER are returned in a feedback buffer, which must be created (see <a href="https://msdn.microsoft.com/fe3773a7-c264-4d49-8f90-1f2319f9af4f">glFeedbackBuffer</a>) before feedback mode is entered.

</td>
</tr>
</table>
 


## -remarks



The <b>glRenderMode</b> function takes one argument, <i>mode</i>, which can assume one of three predefined values above.

The return value of the <b>glRenderMode</b> function is determined by the render mode at the time <b>glRenderMode</b> is called, rather than by <i>mode</i>. The values returned for the three render modes are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GL_RENDER</td>
<td>Zero.</td>
</tr>
<tr>
<td>GL_SELECT</td>
<td>The number of hit records transferred to the select buffer.</td>
</tr>
<tr>
<td>GL_FEEDBACK</td>
<td>The number of values (not vertices) transferred to the feedback buffer.</td>
</tr>
</table>
 

Refer to <a href="https://msdn.microsoft.com/b5c64364-1f47-4281-96b5-95c3f5c8e753">glSelectBuffer</a> and <a href="https://msdn.microsoft.com/fe3773a7-c264-4d49-8f90-1f2319f9af4f">glFeedbackBuffer</a> for more details concerning selection and feedback operation.

If an error is generated, <b>glRenderMode</b> returns zero regardless of the current render mode.

The following function retrieves information related to <b>glRenderMode</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_RENDER_MODE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/fe3773a7-c264-4d49-8f90-1f2319f9af4f">glFeedbackBuffer</a>



<a href="https://msdn.microsoft.com/26c134f5-c17c-4637-93b6-5293f316dd6c">glInitNames</a>



<a href="https://msdn.microsoft.com/8d7d582b-3743-401e-af71-28034e49f3c2">glLoadName</a>



<a href="https://msdn.microsoft.com/14664ac6-eb25-46ae-86d8-7ece31df103f">glPassThrough</a>



<a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a>



<a href="https://msdn.microsoft.com/b5c64364-1f47-4281-96b5-95c3f5c8e753">glSelectBuffer</a>
 

 

