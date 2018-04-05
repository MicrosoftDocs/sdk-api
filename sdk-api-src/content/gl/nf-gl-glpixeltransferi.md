---
UID: NF:gl.glPixelTransferi
title: glPixelTransferi function
author: windows-driver-content
description: The glPixelTransferf and glPixelTransferi functions set pixel transfer modes.
old-location: opengl\glpixeltransferi.htm
old-project: OpenGL
ms.assetid: 351a872d-2cce-4fb1-b736-72201baf4157
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glPixelTransferi, glPixelTransferi, glPixelTransferi function [OpenGL], opengl.glpixeltransferi
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
-	Opengl32.dll
api_name:
-	glPixelTransferi
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPixelTransferi function


## -description


The <a href="https://msdn.microsoft.com/c18ecbb9-af2a-4662-8e3f-0ac850b04fc1">glPixelTransferf</a> and <b>glPixelTransferi</b> functions set pixel transfer modes.


## -parameters




### -param pname

The symbolic name of the pixel transfer parameter to be set. The following table gives the type, initial value, and range of valid values for each of the pixel transfer parameters that are set with <b>glPixelTransfer</b>.

<table>
<tr>
<th>Pname</th>
<th>Type </th>
<th>Initial Value </th>
<th>Valid Range </th>
</tr>
<tr>
<td>GL_MAP_COLOR</td>
<td>Boolean</td>
<td>false</td>
<td>true/false</td>
</tr>
<tr>
<td>GL_MAP_STENCIL</td>
<td>Boolean</td>
<td>false</td>
<td>true/false</td>
</tr>
<tr>
<td>GL_INDEX_SHIFT</td>
<td>integer</td>
<td>0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_INDEX_OFFSET</td>
<td>integer</td>
<td>0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_RED_SCALE</td>
<td>integer</td>
<td>1.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_GREEN_SCALE</td>
<td>float</td>
<td>1.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_BLUE_SCALE</td>
<td>float</td>
<td>1.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_ALPHA_SCALE</td>
<td>float</td>
<td>1.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_DEPTH_SCALE</td>
<td>float</td>
<td>1.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_RED_BIAS</td>
<td>float</td>
<td>0.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_GREEN_BIAS</td>
<td>float</td>
<td>0.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_BLUE_BIAS</td>
<td>float</td>
<td>0.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_ALPHA_BIAS</td>
<td>float</td>
<td>0.0</td>
<td>(∞,∞)</td>
</tr>
<tr>
<td>GL_DEPTH_BIAS</td>
<td>float</td>
<td>0.0</td>
<td>(∞,∞)</td>
</tr>
</table>
 


### -param param

The value that <i>pname</i> is set to.


## -returns



This function does not return a value.




## -remarks



The <b>glPixelTransfer</b> function sets pixel transfer modes that affect the operation of subsequent <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>, <a href="https://msdn.microsoft.com/3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd">glCopyTexImage1D</a>, <a href="https://msdn.microsoft.com/4b9d7be6-054d-4590-b3f0-a2a670786c4b">glCopyTexImage2D</a>, <a href="https://msdn.microsoft.com/718aee8a-6dce-49e1-a441-19beccd89f8d">glCopyTexSubImage1D</a>, <a href="https://msdn.microsoft.com/cbb644d4-6a23-4d66-8599-5f8b48e9b91f">glCopyTexSubImage2D</a>, <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>, <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>, <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>, <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>, <a href="https://msdn.microsoft.com/e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac">glTexSubImage1D</a>, and <a href="https://msdn.microsoft.com/2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7">glTexSubImage2D</a> commands. The algorithms that are specified by pixel transfer modes operate on pixels after they are read from the framebuffer (<b>glReadPixels</b> and <b>glCopyPixels</b>) or unpacked from client memory (<b>glDrawPixels</b>, <b>glTexImage1D</b>, and <b>glTexImage2D</b>). Pixel transfer operations happen in the same order, and in the same manner, regardless of the command that resulted in the pixel operation. Pixel storage modes (<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>) control the unpacking of pixels being read from client memory, and the packing of pixels being written back into client memory.

Pixel transfer operations handle four fundamental pixel types: <i>color</i>, <i>color index</i>, <i>depth</i>, and <i>stencil</i>.Color pixels are made up of four floating-point values with unspecified mantissa and exponent sizes, scaled such that 0.0 represents zero intensity and 1.0 represents full intensity. Color indexes comprise a single fixed-point value, with unspecified precision to the right of the binary point. Depth pixels comprise a single floating-point value, with unspecified mantissa and exponent sizes, scaled such that 0.0 represents the minimum depth buffer value, and 1.0 represents the maximum depth buffer value. Finally, stencil pixels comprise a single fixed-point value, with unspecified precision to the right of the binary point.

The pixel transfer operations performed on the four basic pixel types are as follows:

<table>
<tr>
<th>Pixel type</th>
<th>Pixel transfer operation</th>
</tr>
<tr>
<td>Color</td>
<td>
Each of the four color components is multiplied by a scale factor, and then added to a bias factor. That is, the red component is multiplied by GL_RED_SCALE, and then added to GL_RED_BIAS; the green component is multiplied by GL_GREEN_SCALE, and then added to GL_GREEN_BIAS; the blue component is multiplied by GL_BLUE_SCALE, and then added to GL_BLUE_BIAS; and the alpha component is multiplied by GL_ALPHA_SCALE, and then added to GL_ALPHA_BIAS. After all four color components are scaled and biased, each is clamped to the range [0,1]. All color scale and bias values are specified with <b>glPixelTransfer</b>. 

If GL_MAP_COLOR is true, each color component is scaled by the size of the corresponding color-to-color map, and then replaced by the contents of that map indexed by the scaled component. That is, the red component is scaled by GL_PIXEL_MAP_R_TO_R_SIZE, and then replaced by the contents of GL_PIXEL_MAP_R_TO_R indexed by itself. The green component is scaled by GL_PIXEL_MAP_G_TO_G_SIZE, and then replaced by the contents of GL_PIXEL_MAP_G_TO_G indexed by itself. The blue component is scaled by GL_PIXEL_MAP_B_TO_B_SIZE, and then replaced by the contents of GL_PIXEL_MAP_B_TO_B indexed by itself. The alpha component is scaled by GL_PIXEL_MAP_A_TO_A_SIZE, and then replaced by the contents of GL_PIXEL_MAP_A_TO_A indexed by itself. All components taken from the maps are then clamped to the range [0,1]. GL_MAP_COLOR is specified with <b>glPixelTransfer</b>. The contents of the various maps are specified with <b>glPixelMap</b>.

</td>
</tr>
<tr>
<td>Color index</td>
<td>
Each color index is shifted left by GL_INDEX_SHIFT bits, filling with zeros any bits beyond the number of fraction bits carried by the fixed-point index. If GL_INDEX_SHIFT is negative, the shift is to the right, again zero filled. GL_INDEX_OFFSET is then added to the index. GL_INDEX_SHIFT and GL_INDEX_OFFSET are specified with <b>glPixelTransfer</b>.

From this point, operation diverges depending on the required format of the resulting pixels. If the resulting pixels are to be written to a color-index buffer, or if they are being read back to client memory in GL_COLOR_INDEX format, the pixels continue to be treated as indexes. If GL_MAP_COLOR is true, then each index is masked by 2 ^ <i>n</i> 1, where <i>n</i> is GL_PIXEL_MAP_I_TO_I_SIZE, and then replaced by the contents of GL_PIXEL_MAP_I_TO_I indexed by the masked value. GL_MAP_COLOR is specified with <b>glPixelTransfer</b>. The contents of the index map are specified with <b>glPixelMap</b>.

If the resulting pixels are to be written to an RGBA color buffer, or if they are being read back to client memory in a format other than GL_COLOR_INDEX, the pixels are converted from indexes to colors by referencing the four maps GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_B, and GL_PIXEL_MAP_I_TO_A. Before being dereferenced, the index is masked by 2 n 1, where n is GL_PIXEL_MAP_I_TO_R_SIZE for the red map, GL_PIXEL_MAP_I_TO_G_SIZE for the green map, GL_PIXEL_MAP_I_TO_B_SIZE for the blue map, and GL_PIXEL_MAP_I_TO_A_SIZE for the alpha map. All components taken from the maps are then clamped to the range [0,1]. The contents of the four maps are specified with <b>glPixelMap</b>.

</td>
</tr>
<tr>
<td>Depth</td>
<td>Each depth value is multiplied by GL_DEPTH_SCALE, added to GL_DEPTH_BIAS, and then clamped to the range [0,1].</td>
</tr>
<tr>
<td>Stencil</td>
<td>Each index is shifted GL_INDEX_SHIFT bits just as a color index is, and then added to GL_INDEX_OFFSET. If GL_MAP_STENCIL is true, each index is masked by 2ⁿ 1, where <i>n</i> is GL_PIXEL_MAP_S_TO_S_SIZE, then replaced by the contents of GL_PIXEL_MAP_S_TO_S indexed by the masked value.</td>
</tr>
</table>
 

The <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransferf</a> function can be used to set any pixel transfer parameter. If the parameter type is Boolean, 0.0 implies false and any other value implies true. If <i>pname</i> is an integer parameter, <i>param</i> is rounded to the nearest integer.

Likewise, <b>glPixelTransferi</b> can also be used to set any of the pixel transfer parameters. Boolean parameters are set to false if <i>param</i> is 0 and true otherwise. The <i>param</i> parameter is converted to floating point before being assigned to real-valued parameters.

If a <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>, <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>, <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>, <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>, or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a> command is placed in a display list (see <a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a> and <a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>), the pixel transfer mode settings in effect when the display list is <i>executed</i> are the ones that are used. They may be different from the settings when the command was compiled into the display list.

The following functions retrieve information related to <b>glPixelTransfer</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAP_COLOR

<b>glGet</b> with argument GL_MAP_STENCIL

<b>glGet</b> with argument GL_INDEX_SHIFT

<b>glGet</b> with argument GL_INDEX_OFFSET

<b>glGet</b> with argument GL_RED_SCALE

<b>glGet</b> with argument GL_RED_BIAS

<b>glGet</b> with argument GL_GREEN_SCALE

<b>glGet</b> with argument GL_GREEN_BIAS

<b>glGet</b> with argument GL_BLUE_SCALE

<b>glGet</b> with argument GL_BLUE_BIAS

<b>glGet</b> with argument GL_ALPHA_SCALE

<b>glGet</b> with argument GL_ALPHA_BIAS

<b>glGet</b> with argument GL_DEPTH_SCALE

<b>glGet</b> with argument GL_DEPTH_BIAS




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>



<a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/57ead7d8-0502-46b4-9f66-dbb3cb75b0f9">glPixelZoom</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>
 

 

