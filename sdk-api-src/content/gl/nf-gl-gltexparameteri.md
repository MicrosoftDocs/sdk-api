---
UID: NF:gl.glTexParameteri
title: glTexParameteri function
author: windows-driver-content
description: Sets texture parameters.
old-location: opengl\gltexparameteri.htm
old-project: OpenGL
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_TEXTURE_MAG_FILTER, GL_TEXTURE_MIN_FILTER, GL_TEXTURE_WRAP_S, GL_TEXTURE_WRAP_T, gl/glTexParameteri, glTexParameteri, glTexParameteri function [OpenGL], opengl.gltexparameteri
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
-	glTexParameteri
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glTexParameteri function


## -description


Sets texture parameters.


## -parameters




### -param target

The target texture, which must be either GL_TEXTURE_1D or GL_TEXTURE_2D.


### -param pname

The symbolic name of a single valued texture parameter. The following symbols are accepted in <i>pname</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_MIN_FILTER"></a><a id="gl_texture_min_filter"></a><dl>
<dt><b>GL_TEXTURE_MIN_FILTER</b></dt>
</dl>
</td>
<td width="60%">
The texture minifying function is used whenever the pixel being textured maps to an area greater than one texture element. There are six defined minifying functions. Two of them use the nearest one or nearest four texture elements to compute the texture value. The other four use mipmaps. 


A mipmap is an ordered set of arrays representing the same image at progressively lower resolutions. If the texture has dimensions 2ⁿx2<sup>m</sup> there are max(n, m) + 1 mipmaps. The first mipmap is the original texture, with dimensions 2ⁿx2<sup>m</sup>. Each subsequent mipmap has dimensions 2<sup>k</sup>1x2<sup>l</sup>1 where 2<sup>k</sup>x2<sup>l</sup> are the dimensions of the previous mipmap, until either k = 0 or l = 0. At that point, subsequent mipmaps have dimension 1x2<sup>l</sup>1 or 2<sup>k</sup>1x1 until the final mipmap, which has dimension 1x1. Mipmaps are defined using <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a> with the level-of-detail argument indicating the order of the mipmaps. Level 0 is the original texture; level bold max(n, m) is the final 1x1 mipmap.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_MAG_FILTER"></a><a id="gl_texture_mag_filter"></a><dl>
<dt><b>GL_TEXTURE_MAG_FILTER</b></dt>
</dl>
</td>
<td width="60%">
The texture magnification function is used when the pixel being textured maps to an area less than or equal to one texture element. It sets the texture magnification function to either GL_NEAREST or GL_LINEAR.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_WRAP_S"></a><a id="gl_texture_wrap_s"></a><dl>
<dt><b>GL_TEXTURE_WRAP_S</b></dt>
</dl>
</td>
<td width="60%">
Sets the wrap parameter for texture coordinate s to either GL_CLAMP or GL_REPEAT. GL_CLAMP causes s coordinates to be clamped to the range [0,1] and is useful for preventing wrapping artifacts when mapping a single image onto an object. GL_REPEAT causes the integer part of the s coordinate to be ignored; OpenGL uses only the fractional part, thereby creating a repeating pattern. Border texture elements are accessed only if wrapping is set to GL_CLAMP. Initially, GL_TEXTURE_WRAP_S is set to GL_REPEAT.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_WRAP_T"></a><a id="gl_texture_wrap_t"></a><dl>
<dt><b>GL_TEXTURE_WRAP_T</b></dt>
</dl>
</td>
<td width="60%">
Sets the wrap parameter for texture coordinate t to either GL_CLAMP or GL_REPEAT. See the discussion under GL_TEXTURE_WRAP_S. Initially, GL_TEXTURE_WRAP_T is set to GL_REPEAT

</td>
</tr>
</table>
 


### -param param

The value of <i>pname</i>.


## -returns



This function does not return a value.




## -remarks



Texture mapping is a technique that applies an image onto an object's surface as if the image were a decal or cellophane shrink-wrap. The image is created in texture space, with an (<i>s</i>, <i>t</i>) coordinate system. A texture is a one- or two-dimensional image and a set of parameters that determine how samples are derived from the image.



The <b>glTexParameter</b> function assigns the value or values in params to the texture parameter specified as pname. The target parameter defines the target texture, either GL_TEXTURE_1D or GL_TEXTURE_2D.



As more texture elements are sampled in the minification process, fewer aliasing artifacts will be apparent. While the GL_NEAREST and GL_LINEAR minification functions can be faster than the other four, they sample only one or four texture elements to determine the texture value of the pixel being rendered and can produce moire patterns or ragged transitions. The default value of GL_TEXTURE_MIN_FILTER is GL_NEAREST_MIPMAP_LINEAR.



Suppose that texturing is enabled (by calling <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> with argument GL_TEXTURE_1D or GL_TEXTURE_2D) and GL_TEXTURE_MIN_FILTER is set to one of the functions that requires a mipmap. If either the dimensions of the texture images currently defined (with previous calls to <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> or <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>) do not follow the proper sequence for mipmaps, or there are fewer texture images defined than are needed, or the set of texture images have differing numbers of texture components, then it is as if texture mapping were disabled. 

Linear filtering accesses the four nearest texture elements only in 2-D textures. In 1-D textures, linear filtering accesses the two nearest texture elements.

The following function retrieves information related to <b>glTexParameterf</b>, <b>glTexParameteri</b>, <b>glTexParameterfv</b>, and <b>glTexParameteriv</b>:


<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>





## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/800f2360-b40e-4911-9a45-6f310aeeefeb">glBindTexture</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd">glCopyTexImage1D</a>



<a href="https://msdn.microsoft.com/4b9d7be6-054d-4590-b3f0-a2a670786c4b">glCopyTexImage2D</a>



<a href="https://msdn.microsoft.com/cbb644d4-6a23-4d66-8599-5f8b48e9b91f">glCopyTexSubImage2D</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/09018c86-c667-4e43-a95a-51a8077aed33">glPrioritizeTextures</a>



<a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac">glTexSubImage1D</a>



<a href="https://msdn.microsoft.com/2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7">glTexSubImage2D</a>
 

 

