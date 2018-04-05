---
UID: NF:gl.glAccum
title: glAccum function
author: windows-driver-content
description: The glAccum function operates on the accumulation buffer.
old-location: opengl\glaccum.htm
old-project: OpenGL
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ACCUM, GL_ADD, GL_LOAD, GL_MULT, GL_RETURN, _ogl_glAccum, gl/glAccum, glAccum, glAccum function [OpenGL], opengl.glaccum
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
-	glAccum
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glAccum function


## -description


The <b>glAccum</b> function operates on the accumulation buffer.


## -parameters




### -param op

The accumulation buffer operation. The accepted symbolic constants are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_ACCUM"></a><a id="gl_accum"></a><dl>
<dt><b>GL_ACCUM</b></dt>
</dl>
</td>
<td width="60%">
Obtains R, G, B, and A values from the buffer currently selected for reading (see <a href="https://msdn.microsoft.com/734153fa-e809-4b70-867e-55e46ab95712">glReadBuffer</a>). Each component value is divided by 2<i>ⁿ</i>  1, where <i>n</i> is the number of bits allocated to each color component in the currently selected buffer. The result is a floating-point value in the range [0,1], which is multiplied by <i>value</i> and added to the corresponding pixel component in the accumulation buffer, thereby updating the accumulation buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LOAD"></a><a id="gl_load"></a><dl>
<dt><b>GL_LOAD</b></dt>
</dl>
</td>
<td width="60%">
Similar to GL_ACCUM, except that the current value in the accumulation buffer is not used in the calculation of the new value. That is, the R, G, B, and A values from the currently selected buffer are divided by 2<i>ⁿ</i>  1, multiplied by <i>value</i>, and then stored in the corresponding accumulation buffer cell, overwriting the current value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ADD"></a><a id="gl_add"></a><dl>
<dt><b>GL_ADD</b></dt>
</dl>
</td>
<td width="60%">
Adds <i>value</i> to each R, G, B, and A in the accumulation buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MULT"></a><a id="gl_mult"></a><dl>
<dt><b>GL_MULT</b></dt>
</dl>
</td>
<td width="60%">
Multiplies each R, G, B, and A in the accumulation buffer by <i>value</i> and returns the scaled component to its corresponding accumulation buffer location.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RETURN"></a><a id="gl_return"></a><dl>
<dt><b>GL_RETURN</b></dt>
</dl>
</td>
<td width="60%">
Transfers accumulation buffer values to the color buffer or buffers currently selected for writing. Each R, G, B, and A component is multiplied by <i>value</i>, then multiplied by 2<i>ⁿ</i>  1, clamped to the range [0, 2<i>ⁿ</i>  1 ], and stored in the corresponding display buffer cell. The only fragment operations that are applied to this transfer are pixel ownership, scissor, dithering, and color writemasks.

</td>
</tr>
</table>
 


### -param value

A floating-point value used in the accumulation buffer operation. The <i>op</i> parameter determines how <i>value</i> is used.


## -returns



This function does not return a value.




## -remarks



The accumulation buffer is an extended-range color buffer. Images are not rendered into it. Rather, images rendered into one of the color buffers are added to the contents of the accumulation buffer after rendering. You can create effects such as antialiasing (of points, lines, and polygons), motion blur, and depth of field by accumulating images generated with different transformation matrices.

Each pixel in the accumulation buffer consists of red, green, blue, and alpha values. The number of bits per component in the accumulation buffer depends on the implementation. You can examine this number by calling <a href="https://msdn.microsoft.com/16b04af6-5da3-439f-8d4f-bc8ab1fcb2c5">glGetIntegerv</a> four times, with the arguments GL_ACCUM_RED_BITS, GL_ACCUM_GREEN_BITS, GL_ACCUM_BLUE_BITS, and GL_ACCUM_ALPHA_BITS, respectively. Regardless of the number of bits per component, however, the range of values stored by each component is [ 1,?1]. The accumulation buffer pixels are mapped one-to-one with framebuffer pixels.

The <b>glAccum</b> function operates on the accumulation buffer. The first argument, <i>op</i>, is a symbolic constant that selects an accumulation buffer operation. The second argument, <i>value</i>, is a floating-point value to be used in that operation. Five operations are specified: GL_ACCUM, GL_LOAD, GL_ADD, GL_MULT, and GL_RETURN.

All accumulation buffer operations are limited to the area of the current scissor box and are applied identically to the red, green, blue, and alpha components of each pixel. The contents of an accumulation buffer pixel component are undefined if the <b>glAccum</b> operation results in a value outside the range [ 1,1].

To clear the accumulation buffer, use the <a href="https://msdn.microsoft.com/77d8f340-be47-43f4-96fc-31025a4c8b4e">glClearAccum</a> function to specify R, G, B, and A values to set it to, and issue a <a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a> function with the accumulation buffer enabled.

Only those pixels within the current scissor box are updated by any <b>glAccum</b> operation.

The following functions retrieve information related to the <b>glAccum</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_ACCUM_RED_BITS

<b>glGet</b> with argument GL_ACCUM_GREEN_BITS

<b>glGet</b> with argument GL_ACCUM_BLUE_BITS

<b>glGet</b> with argument GL_ACCUM_ALPHA_BITS




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>



<a href="https://msdn.microsoft.com/9818f969-3145-45ea-aa9c-2abed953a8e0">glClear</a>



<a href="https://msdn.microsoft.com/77d8f340-be47-43f4-96fc-31025a4c8b4e">glClearAccum</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/734153fa-e809-4b70-867e-55e46ab95712">glReadBuffer</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>



<a href="https://msdn.microsoft.com/c06a1d20-bf7b-4283-b0fe-8bd80bece4ce">glScissor</a>



<a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>
 

 

