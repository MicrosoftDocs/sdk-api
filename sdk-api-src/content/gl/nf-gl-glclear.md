---
UID: NF:gl.glClear
title: glClear function
author: windows-driver-content
description: The glClear function clears buffers to preset values.
old-location: opengl\glclear.htm
old-project: OpenGL
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ACCUM_BUFFER_BIT, GL_COLOR_BUFFER_BIT, GL_DEPTH_BUFFER_BIT, GL_STENCIL_BUFFER_BIT, _ogl_glClear, gl/glClear, glClear, glClear function [OpenGL], opengl.glclear
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
-	glClear
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glClear function


## -description


The <b>glClear</b> function clears buffers to preset values.


## -parameters




### -param mask

Bitwise OR operators of masks that indicate the buffers to be cleared. The four masks are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_BUFFER_BIT"></a><a id="gl_color_buffer_bit"></a><dl>
<dt><b>GL_COLOR_BUFFER_BIT</b></dt>
</dl>
</td>
<td width="60%">
The buffers currently enabled for color writing.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_BUFFER_BIT"></a><a id="gl_depth_buffer_bit"></a><dl>
<dt><b>GL_DEPTH_BUFFER_BIT</b></dt>
</dl>
</td>
<td width="60%">
The depth buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ACCUM_BUFFER_BIT"></a><a id="gl_accum_buffer_bit"></a><dl>
<dt><b>GL_ACCUM_BUFFER_BIT</b></dt>
</dl>
</td>
<td width="60%">
The accumulation buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_BUFFER_BIT"></a><a id="gl_stencil_buffer_bit"></a><dl>
<dt><b>GL_STENCIL_BUFFER_BIT</b></dt>
</dl>
</td>
<td width="60%">
The stencil buffer.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>glClear</b> function sets the bitplane area of the window to values previously selected by <a href="https://msdn.microsoft.com/f938e3f4-9db3-4c24-97ae-531b6799224e">glClearColor</a>, <a href="https://msdn.microsoft.com/87983d93-c5a1-445f-8621-1c2952d93a0f">glClearIndex</a>, <a href="https://msdn.microsoft.com/8e26ae78-edc1-4201-a0db-d5bc8ae6dc82">glClearDepth</a>, <a href="https://msdn.microsoft.com/bbde8fa8-78f3-45bd-bac3-5d03839acc52">glClearStencil</a>, and <a href="https://msdn.microsoft.com/77d8f340-be47-43f4-96fc-31025a4c8b4e">glClearAccum</a>. You can clear multiple color buffers simultaneously by selecting more than one buffer at a time using <a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>.

The pixel-ownership test, the scissor test, dithering, and the buffer writemasks affect the operation of <b>glClear</b>. The scissor box bounds the cleared region. The <b>glClear</b> function ignores the alpha function, blend function, logical operation, stenciling, texture mapping, and <i>z</i>-buffering.

The <b>glClear</b> function takes a single argument (<i>mask</i>) that is the bitwise OR of several values indicating which buffer is to be cleared.

The value to which each buffer is cleared depends on the setting of the clear value for that buffer.

If a buffer is not present, a <b>glClear</b> call directed at that buffer has no effect.

The following functions retrieve information related to <b>glClear</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_ACCUM_CLEAR_VALUE

<b>glGet</b> with argument GL_DEPTH_CLEAR_VALUE

<b>glGet</b> with argument GL_INDEX_CLEAR_VALUE

<b>glGet</b> with argument GL_COLOR_CLEAR_VALUE

<b>glGet</b> with argument GL_STENCIL_CLEAR_VALUE




## -see-also




<a href="https://msdn.microsoft.com/77d8f340-be47-43f4-96fc-31025a4c8b4e">glClearAccum</a>



<a href="https://msdn.microsoft.com/f938e3f4-9db3-4c24-97ae-531b6799224e">glClearColor</a>



<a href="https://msdn.microsoft.com/8e26ae78-edc1-4201-a0db-d5bc8ae6dc82">glClearDepth</a>



<a href="https://msdn.microsoft.com/87983d93-c5a1-445f-8621-1c2952d93a0f">glClearIndex</a>



<a href="https://msdn.microsoft.com/bbde8fa8-78f3-45bd-bac3-5d03839acc52">glClearStencil</a>



<a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/c06a1d20-bf7b-4283-b0fe-8bd80bece4ce">glScissor</a>
 

 

