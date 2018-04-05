---
UID: NF:gl.glLogicOp
title: glLogicOp function
author: windows-driver-content
description: The glLogicOp function specifies a logical pixel operation for color index rendering.
old-location: opengl\gllogicop.htm
old-project: OpenGL
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_AND, GL_AND_INVERTED, GL_AND_REVERSE, GL_CLEAR, GL_COPY, GL_COPY_INVERTED, GL_EQUIV, GL_INVERT, GL_NAND, GL_NOOP, GL_NOR, GL_OR, GL_OR_INVERTED, GL_OR_REVERSE, GL_SET, GL_XOR, _ogl_glLogicOp, gl/glLogicOp, glLogicOp, glLogicOp function [OpenGL], opengl.gllogicop
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
-	glLogicOp
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glLogicOp function


## -description


The <b>glLogicOp</b> function specifies a logical pixel operation for color index rendering.


## -parameters




### -param opcode

A symbolic constant that selects a logical operation. The following symbols are accepted where s equals the value of the source bit and d is the value of the destination bit.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_CLEAR"></a><a id="gl_clear"></a><dl>
<dt><b>GL_CLEAR</b></dt>
</dl>
</td>
<td width="60%">
0

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SET"></a><a id="gl_set"></a><dl>
<dt><b>GL_SET</b></dt>
</dl>
</td>
<td width="60%">
1

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COPY"></a><a id="gl_copy"></a><dl>
<dt><b>GL_COPY</b></dt>
</dl>
</td>
<td width="60%">
s

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COPY_INVERTED"></a><a id="gl_copy_inverted"></a><dl>
<dt><b>GL_COPY_INVERTED</b></dt>
</dl>
</td>
<td width="60%">
!s

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NOOP"></a><a id="gl_noop"></a><dl>
<dt><b>GL_NOOP</b></dt>
</dl>
</td>
<td width="60%">
d

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INVERT"></a><a id="gl_invert"></a><dl>
<dt><b>GL_INVERT</b></dt>
</dl>
</td>
<td width="60%">
!d

</td>
</tr>
<tr>
<td width="40%"><a id="GL_AND"></a><a id="gl_and"></a><dl>
<dt><b>GL_AND</b></dt>
</dl>
</td>
<td width="60%">
s &amp; d

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NAND"></a><a id="gl_nand"></a><dl>
<dt><b>GL_NAND</b></dt>
</dl>
</td>
<td width="60%">
!(s &amp; d)

</td>
</tr>
<tr>
<td width="40%"><a id="GL_OR"></a><a id="gl_or"></a><dl>
<dt><b>GL_OR</b></dt>
</dl>
</td>
<td width="60%">
s | d

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NOR"></a><a id="gl_nor"></a><dl>
<dt><b>GL_NOR</b></dt>
</dl>
</td>
<td width="60%">
!(s | d)

</td>
</tr>
<tr>
<td width="40%"><a id="GL_XOR"></a><a id="gl_xor"></a><dl>
<dt><b>GL_XOR</b></dt>
</dl>
</td>
<td width="60%">
s ^ d

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EQUIV"></a><a id="gl_equiv"></a><dl>
<dt><b>GL_EQUIV</b></dt>
</dl>
</td>
<td width="60%">
!(s ^ d)

</td>
</tr>
<tr>
<td width="40%"><a id="GL_AND_REVERSE"></a><a id="gl_and_reverse"></a><dl>
<dt><b>GL_AND_REVERSE</b></dt>
</dl>
</td>
<td width="60%">
s &amp; !d

</td>
</tr>
<tr>
<td width="40%"><a id="GL_AND_INVERTED"></a><a id="gl_and_inverted"></a><dl>
<dt><b>GL_AND_INVERTED</b></dt>
</dl>
</td>
<td width="60%">
!s &amp; d

</td>
</tr>
<tr>
<td width="40%"><a id="GL_OR_REVERSE"></a><a id="gl_or_reverse"></a><dl>
<dt><b>GL_OR_REVERSE</b></dt>
</dl>
</td>
<td width="60%">
s | !d

</td>
</tr>
<tr>
<td width="40%"><a id="GL_OR_INVERTED"></a><a id="gl_or_inverted"></a><dl>
<dt><b>GL_OR_INVERTED</b></dt>
</dl>
</td>
<td width="60%">
!s | d

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>glLogicOp</b> function specifies a logical operation that, when enabled, is applied between the incoming color index and the color index at the corresponding location in the framebuffer. The logical operation is enabled or disabled with <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> using the symbolic constant GL_LOGIC_OP.

The <i>opcode</i> parameter is a symbolic constant chosen from the list below. In the explanation of the logical operations, <i>s</i> represents the incoming color index and <i>d</i> represents the index in the framebuffer. Standard C-language operators are used. As these bitwise operators suggest, the logical operation is applied independently to each bit pair of the source and destination indexes.

Logical pixel operations are not applied to RGBA color buffers.

When more than one color-index buffer is enabled for drawing, logical operations are done separately for each enabled buffer, using the contents of that buffer for the destination index (see <a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>).

The <i>opcode</i> parameter must be one of the 16 accepted values. Other values result in an error.

The following functions retrieve information related to <b>glLogicOp</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_LOGIC_OP_MODE


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_LOGIC_OP




## -see-also




<a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>



<a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>
 

 

