---
UID: NF:gl.glPixelStoref
title: glPixelStoref function
author: windows-driver-content
description: Sets pixel storage modes.
old-location: opengl\glpixelstoref.htm
old-project: OpenGL
ms.assetid: 8d5055d7-3ea4-40b7-9447-2a005129da58
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glPixelStoref, glPixelStoref, glPixelStoref function [OpenGL], opengl.glpixelstoref
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
-	glPixelStoref
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPixelStoref function


## -description


Sets pixel storage modes.


## -parameters




### -param pname

The symbolic name of the parameter to be set. Six of the storage parameters affect how pixel data is returned to client memory, and are therefore significant only for <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a> commands. They are as follows:
			 

<table>
<tr>
<th>Storage Parameter</th>
<th>Description</th>
</tr>
<tr>
<td>GL_PACK_SWAP_BYTES</td>
<td>If true, byte ordering for multibyte color components, depth components, color indexes, or stencil indexes is reversed. That is, if a four-byte component is made up of bytes <i>b</i>₀ , <i>b</i>₁ , <i>b</i>₂ , <i>b</i>₃ , it is stored in memory as <i>b</i>₃ , <i>b</i>₂ , <i>b</i>₁ , <i>b</i>₀ if GL_PACK_SWAP_BYTES is true. GL_PACK_SWAP_BYTES has no effect on the memory order of components within a pixel, only on the order of bytes within components or indexes. For example, the three components of a GL_RGB format pixel are always stored with red first, green second, and blue third, regardless of the value of GL_PACK_SWAP_BYTES.</td>
</tr>
<tr>
<td>GL_PACK_LSB_FIRST</td>
<td>If true, bits are ordered within a byte from least significant to most significant; otherwise, the first bit in each byte is the most significant one. This parameter is significant for bitmap data only.</td>
</tr>
<tr>
<td>GL_PACK_ROW_LENGTH</td>
<td>If greater than zero, GL_PACK_ROW_LENGTH defines the number of pixels in a row. If the first pixel of a row is placed at location p in memory, then the location of the first pixel of the next row is obtained by skipping
<img alt="" border="0" src="images/pix01.png"/></p>          
          components or indexes, where <i>n</i> is the number of components or indexes in a pixel, <i>l</i> is the number of pixels in a row (GL_PACK_ROW_LENGTH if it is greater than zero, the width argument to the pixel routine otherwise), <i>a</i> is the value of GL_PACK_ALIGNMENT, and <i>s</i> is the size, in bytes, of a single component (if <i>a</i> &lt; <i>s</i>, then it is as if <i>a</i> = <i>s</i>). In the case of 1-bit values, the location of the next row is obtained by skipping
         <img alt="" border="0" src="images/pix02.png"/>

          components or indexes.
          The word <i>component</i> in this description refers to the nonindex values red, green, blue, alpha, and depth. Storage format GL_RGB, for example, has three components per pixel: first red, then green, and finally blue.

</td>
</tr>
<tr>
<td>GL_PACK_SKIP_PIXELS and 

</p>GL_PACK_SKIP_ROWS</td>
<td>These values are provided as a convenience to the programmer; they provide no functionality that cannot be duplicated simply by incrementing the pointer passed to <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>. Setting GL_PACK_SKIP_PIXELS to <i>i</i> is equivalent to incrementing the pointer by <i>i n</i> components or indexes, where <i>n</i> is the number of components or indexes in each pixel. Setting GL_PACK_SKIP_ROWS to <i>j</i> is equivalent to incrementing the pointer by <i>j k</i> components or indexes, where <i>k</i> is the number of components or indexes per row, as computed above in the GL_PACK_ROW_LENGTH section.</td>
</tr>
<tr>
<td>GL_PACK_ALIGNMENT</td>
<td>Specifies the alignment requirements for the start of each pixel row in memory. The allowable values are 1 (byte-alignment), 2 (rows aligned to even-numbered bytes), 4 (word alignment), and 8 (rows start on double-word boundaries).</td>
</tr>
</table>
 

The other six storage parameters affect how pixel data is read from client memory. These values are significant for <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>, <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>, <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>, <a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>, and <a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>. They are as follows:

<table>
<tr>
<th>Storage Parameter</th>
<th>Description</th>
</tr>
<tr>
<td>GL_UNPACK_SWAP_BYTES</td>
<td>If true, byte ordering for multibyte color components, depth components, color indexes, or stencil indexes is reversed. That is, if a four-byte component is made up of bytes <i>b</i>₀ , <i>b</i>₁ , <i>b</i>₂ , <i>b</i>₃ , it is stored in memory as <i>b</i>₃ , <i>b</i>₂ , <i>b</i>₁ , <i>b</i>₀ if GL_UNPACK_SWAP_BYTES is true. GL_UNPACK_SWAP_BYTES has no effect on the memory order of components within a pixel, only on the order of bytes within components or indexes. For example, the three components of a GL_RGB format pixel are always stored with red first, green second, and blue third, regardless of the value of GL_UNPACK_SWAP_BYTES.</td>
</tr>
<tr>
<td>GL_UNPACK_LSB_FIRST</td>
<td>If true, bits are ordered within a byte from least significant to most significant; otherwise, the first bit in each byte is the most significant one. This is significant for bitmap data only.</td>
</tr>
<tr>
<td>GL_UNPACK_ROW_LENGTH</td>
<td>If greater than zero, GL_UNPACK_ROW_LENGTH defines the number of pixels in a row. If the first pixel of a row is placed at location p in memory, then the location of the first pixel of the next row is obtained by skipping
<img alt="" border="0" src="images/pix01.png"/></p>          
          components or indexes, where <i>n</i> is the number of components or indexes in a pixel, <i>l</i> is the number of pixels in a row (GL_PACK_ROW_LENGTH if it is greater than zero, the width argument to the pixel routine otherwise), <i>a</i> is the value of GL_PACK_ALIGNMENT, and <i>s</i> is the size, in bytes, of a single component (if <i>a</i> &lt; <i>s</i>, then it is as if <i>a</i> = <i>s</i>). In the case of 1-bit values, the location of the next row is obtained by skipping
         <img alt="" border="0" src="images/pix02.png"/>

          components or indexes.
          The word <i>component</i> in this description refers to the nonindex values red, green, blue, alpha, and depth. Storage format GL_RGB, for example, has three components per pixel: first red, then green, and finally blue.

</td>
</tr>
<tr>
<td>GL_UNPACK_SKIP_PIXELS and 

</p>GL_UNPACK_SKIP_ROWS</td>
<td>These values are provided as a convenience to the programmer; they provide no functionality that cannot be duplicated simply by incrementing the pointer passed to <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>, <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>, <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>, <a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>, or <a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>. Setting GL_UNPACK_SKIP_PIXELS to <i>i</i> is equivalent to incrementing the pointer by <i>i n</i> components or indexes, where <i>n</i> is the number of components or indexes in each pixel. Setting GL_UNPACK_SKIP_ROWS to <i>j</i> is equivalent to incrementing the pointer by <i>j k</i> components or indexes, where <i>k</i> is the number of components or indexes per row, as computed above in the GL_UNPACK_ROW_LENGTH section.</td>
</tr>
<tr>
<td>GL_UNPACK_ALIGNMENT</td>
<td>Specifies the alignment requirements for the start of each pixel row in memory. The allowable values are 1 (byte-alignment), 2 (rows aligned to even-numbered bytes), 4 (word alignment), and 8 (rows start on double-word boundaries).</td>
</tr>
</table>
 


### -param param

The value that <i>pname</i> is set to.


## -returns



This function does not return a value.




## -remarks



The <b>glPixelStore</b> function sets pixel storage modes that affect the operation of subsequent <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a> and <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a> as well as the unpacking of polygon stipple patterns (see <a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>), bitmaps (see <a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>), and texture patterns (see <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>, <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>, <a href="https://msdn.microsoft.com/e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac">glTexSubImage1D</a>, and <a href="https://msdn.microsoft.com/2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7">glTexSubImage2D</a>).

The following table gives the type, initial value, and range of valid values for each of the storage parameters that can be set with <b>glPixelStore</b>.

<table>
<tr>
<th>Pname</th>
<th>Type</th>
<th>Initial Value</th>
<th>Valid Range</th>
</tr>
<tr>
<td>GL_PACK_SWAP_BYTES</td>
<td>Boolean</td>
<td>false</td>
<td>true or false</td>
</tr>
<tr>
<td>GL_PACK_SWAP_BYTES</td>
<td>Boolean</td>
<td>false</td>
<td>true or false</td>
</tr>
<tr>
<td>GL_PACK_ROW_LENGTH</td>
<td>integer</td>
<td>0</td>
<td>[0,?)</td>
</tr>
<tr>
<td>GL_PACK_SKIP_ROWS</td>
<td>integer</td>
<td>0</td>
<td>[0,?)</td>
</tr>
<tr>
<td>GL_PACK_SKIP_PIXELS</td>
<td>integer</td>
<td>0</td>
<td>[0,?)</td>
</tr>
<tr>
<td>GL_PACK_ALIGNMENT</td>
<td>integer</td>
<td>4</td>
<td>1, 2, 4, or 8</td>
</tr>
<tr>
<td>GL_UNPACK_SWAP_BYTES</td>
<td>Boolean</td>
<td>false</td>
<td>true or false</td>
</tr>
<tr>
<td>GL_UNPACK_LSB_FIRST</td>
<td>Boolean</td>
<td>false</td>
<td>true or false</td>
</tr>
<tr>
<td>GL_UNPACK_ROW_LENGTH</td>
<td>integer</td>
<td>0</td>
<td>[0,?)</td>
</tr>
<tr>
<td>GL_UNPACK_SKIP_ROWS</td>
<td>integer</td>
<td>0</td>
<td>[0,?)</td>
</tr>
<tr>
<td>GL_UNPACK_SKIP_PIXELS</td>
<td>integer</td>
<td>0</td>
<td>[0,?)</td>
</tr>
<tr>
<td>GL_UNPACK_ALIGNMENT</td>
<td>integer</td>
<td>4</td>
<td>1, 2, 4, or 8</td>
</tr>
</table>
 

The <b>glPixelStoref</b> function can be used to set any pixel store parameter. If the parameter type is Boolean, and if <i>param</i> is 0.0, then the parameter is false; otherwise it is set to true. If <i>pname</i> is an integer type parameter, then <i>param</i> is rounded to the nearest integer.

Likewise, the <b>glPixelStorei</b> function can also be used to set any of the pixel store parameters. Boolean parameters are set to false if <i>param</i> is 0 and true otherwise. The <i>param</i> parameter is converted to floating point before being assigned to real-valued parameters.

The pixel storage modes in effect when <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>, <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>, <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>, <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>, <a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>, or <a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a> is placed in a display list control the interpretation of memory data. The pixel storage modes in effect when a display list is executed are not significant.

The following functions retrieve information related to <b>glPixelStore</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_PACK_SWAP_BYTES

<b>glGet</b> with argument GL_PACK_LSB_FIRST

<b>glGet</b> with argument GL_PACK_ROW_LENGTH

<b>glGet</b> with argument GL_PACK_SKIP_ROWS

<b>glGet</b> with argument GL_PACK_SKIP_PIXELS

<b>glGet</b> with argument GL_PACK_ALIGNMENT

<b>glGet</b> with argument GL_UNPACK_SWAP_BYTES

<b>glGet</b> with argument GL_UNPACK_LSB_FIRST

<b>glGet</b> with argument GL_UNPACK_ROW_LENGTH

<b>glGet</b> with argument GL_UNPACK_SKIP_ROWS

<b>glGet</b> with argument GL_UNPACK_SKIP_PIXELS

<b>glGet</b> with argument GL_UNPACK_ALIGNMENT




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/57ead7d8-0502-46b4-9f66-dbb3cb75b0f9">glPixelZoom</a>



<a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>
 

 

