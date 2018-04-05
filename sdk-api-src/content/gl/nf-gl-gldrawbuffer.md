---
UID: NF:gl.glDrawBuffer
title: glDrawBuffer function
author: windows-driver-content
description: The glDrawBuffer function specifies which color buffers are to be drawn into.
old-location: opengl\gldrawbuffer.htm
old-project: OpenGL
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_AUXi, GL_BACK, GL_BACK_LEFT, GL_BACK_RIGHT, GL_FRONT, GL_FRONT_AND_BACK, GL_FRONT_LEFT, GL_FRONT_RIGHT, GL_LEFT, GL_NONE, GL_RIGHT, _ogl_glDrawBuffer, gl/glDrawBuffer, glDrawBuffer, glDrawBuffer function [OpenGL], opengl.gldrawbuffer
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
-	glDrawBuffer
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glDrawBuffer function


## -description


The <b>glDrawBuffer</b> function specifies which color buffers are to be drawn into.


## -parameters




### -param mode

Specifies up to four color buffers to be drawn into with the following acceptable symbolic constants.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_NONE"></a><a id="gl_none"></a><dl>
<dt><b>GL_NONE</b></dt>
</dl>
</td>
<td width="60%">
No color buffers are written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FRONT_LEFT"></a><a id="gl_front_left"></a><dl>
<dt><b>GL_FRONT_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Only the front-left color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FRONT_RIGHT"></a><a id="gl_front_right"></a><dl>
<dt><b>GL_FRONT_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Only the front-right color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BACK_LEFT"></a><a id="gl_back_left"></a><dl>
<dt><b>GL_BACK_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Only the back-left color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BACK_RIGHT"></a><a id="gl_back_right"></a><dl>
<dt><b>GL_BACK_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Only the back-right color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FRONT"></a><a id="gl_front"></a><dl>
<dt><b>GL_FRONT</b></dt>
</dl>
</td>
<td width="60%">
Only the front-left and front-right color buffers are written. If there is no front-right color buffer, only the front left-color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BACK"></a><a id="gl_back"></a><dl>
<dt><b>GL_BACK</b></dt>
</dl>
</td>
<td width="60%">
Only the back-left and back-right color buffers are written. If there is no back-right color buffer, only the back-left color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LEFT"></a><a id="gl_left"></a><dl>
<dt><b>GL_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Only the front-left and back-left color buffers are written. If there is no back-left color buffer, only the front-left color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RIGHT"></a><a id="gl_right"></a><dl>
<dt><b>GL_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Only the front-right and back-right color buffers are written. If there is no back-right color buffer, only the front-right color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FRONT_AND_BACK"></a><a id="gl_front_and_back"></a><dl>
<dt><b>GL_FRONT_AND_BACK</b></dt>
</dl>
</td>
<td width="60%">
All the front and back color buffers (front-left, front-right, back-left, back-right) are written. If there are no back color buffers, only the front-left and front-right color buffers are written. If there are no right color buffers, only the front-left and back-left color buffers are written. If there are no right or back color buffers, only the front-left color buffer is written.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_AUXi"></a><a id="gl_auxi"></a><a id="GL_AUXI"></a><dl>
<dt><b>GL_AUXi</b></dt>
</dl>
</td>
<td width="60%">
Only the auxiliary color buffer <i>i</i> is written; <i>i</i> is between 0 and GL_AUX_BUFFERS - 1. (GL_AUX_BUFFERS is not the upper limit; use <a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> to query the number of available auxiliary buffers.)

</td>
</tr>
</table>
 

The default value is GL_FRONT for single-buffered contexts, and GL_BACK for double-buffered contexts.


## -returns



This function does not return a value.




## -remarks



When colors are written to the framebuffer, they are written into the color buffers specified by <b>glDrawBuffer</b>.

If more than one color buffer is selected for drawing, then blending or logical operations are computed and applied independently for each color buffer and can produce different results in each buffer.

Monoscopic contexts include only left buffers, and stereoscopic contexts include both left and right buffers. Likewise, single-buffered contexts include only front buffers, and double-buffered contexts include both front and back buffers. The context is selected at OpenGL initialization.

It is always the case that GL_AUX <i>i</i> = GL_AUX0 + <i>i</i>.

The following functions retrieve information related to the <b>glDrawBuffer</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_DRAW_BUFFER

<b>glGet</b> with argument GL_AUX_BUFFERS




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>



<a href="https://msdn.microsoft.com/23d7f94e-f290-423c-a841-f86caf94009d">glColorMask</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/f4b5df36-390f-4254-95fb-98589750a11b">glIndexMask</a>



<a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>



<a href="https://msdn.microsoft.com/734153fa-e809-4b70-867e-55e46ab95712">glReadBuffer</a>
 

 

