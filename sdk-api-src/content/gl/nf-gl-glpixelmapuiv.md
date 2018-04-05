---
UID: NF:gl.glPixelMapuiv
title: glPixelMapuiv function
author: windows-driver-content
description: The glPixelMapuiv function sets up pixel transfer maps.
old-location: opengl\glpixelmapuiv.htm
old-project: OpenGL
ms.assetid: dd0f7881-fdd1-49c2-b68c-21e2f9e5ecd2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_PIXEL_MAP_A_TO_A, GL_PIXEL_MAP_B_TO_B, GL_PIXEL_MAP_G_TO_G, GL_PIXEL_MAP_I_TO_A, GL_PIXEL_MAP_I_TO_B, GL_PIXEL_MAP_I_TO_G, GL_PIXEL_MAP_I_TO_I, GL_PIXEL_MAP_I_TO_R, GL_PIXEL_MAP_R_TO_R, GL_PIXEL_MAP_S_TO_S, gl/glPixelMapuiv, glPixelMapuiv, glPixelMapuiv function [OpenGL], opengl.glpixelmapuiv
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
-	glPixelMapuiv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPixelMapuiv function


## -description


The <b>glPixelMapuiv</b> function sets up pixel transfer maps.


## -parameters




### -param map

A symbolic map name. The ten maps are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_I"></a><a id="gl_pixel_map_i_to_i"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_I</b></dt>
</dl>
</td>
<td width="60%">
Maps color indexes to color indexes.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_S_TO_S"></a><a id="gl_pixel_map_s_to_s"></a><dl>
<dt><b>GL_PIXEL_MAP_S_TO_S</b></dt>
</dl>
</td>
<td width="60%">
Maps stencil indexes to stencil indexes.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_R"></a><a id="gl_pixel_map_i_to_r"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_R</b></dt>
</dl>
</td>
<td width="60%">
Maps color indexes to red components.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_G"></a><a id="gl_pixel_map_i_to_g"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_G</b></dt>
</dl>
</td>
<td width="60%">
Maps color indexes to green components.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_B"></a><a id="gl_pixel_map_i_to_b"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_B</b></dt>
</dl>
</td>
<td width="60%">
Maps color indexes to blue components.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_A"></a><a id="gl_pixel_map_i_to_a"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_A</b></dt>
</dl>
</td>
<td width="60%">
Maps color indexes to alpha components.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_R_TO_R"></a><a id="gl_pixel_map_r_to_r"></a><dl>
<dt><b>GL_PIXEL_MAP_R_TO_R</b></dt>
</dl>
</td>
<td width="60%">
Maps red components to red components.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_G_TO_G"></a><a id="gl_pixel_map_g_to_g"></a><dl>
<dt><b>GL_PIXEL_MAP_G_TO_G</b></dt>
</dl>
</td>
<td width="60%">
Maps green components to green components.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_B_TO_B"></a><a id="gl_pixel_map_b_to_b"></a><dl>
<dt><b>GL_PIXEL_MAP_B_TO_B</b></dt>
</dl>
</td>
<td width="60%">
Maps blue components to blue components.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_A_TO_A"></a><a id="gl_pixel_map_a_to_a"></a><dl>
<dt><b>GL_PIXEL_MAP_A_TO_A</b></dt>
</dl>
</td>
<td width="60%">
Maps alpha components to alpha components.

</td>
</tr>
</table>
 


### -param mapsize

The size of the map being defined.


### -param values

An array of <i>mapsize</i> values.


## -returns



This function does not return a value.




## -remarks



The <b>glPixelMap</b> function sets up translation tables, or <i>maps</i>, used by <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>, <a href="https://msdn.microsoft.com/3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd">glCopyTexImage1D</a>, <a href="https://msdn.microsoft.com/4b9d7be6-054d-4590-b3f0-a2a670786c4b">glCopyTexImage2D</a>, <a href="https://msdn.microsoft.com/718aee8a-6dce-49e1-a441-19beccd89f8d">glCopyTexSubImage1D</a>, <a href="https://msdn.microsoft.com/cbb644d4-6a23-4d66-8599-5f8b48e9b91f">glCopyTexSubImage2D</a>, <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>, <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>, <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>, <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>, <a href="https://msdn.microsoft.com/e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac">glTexSubImage1D</a>, and <a href="https://msdn.microsoft.com/2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7">glTexSubImage2D</a>. Use of these maps is described completely in the <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a> topic, and partly in the topics for the pixel and texture image commands. Only the specification of the maps is described in this topic.

The <i>map</i> parameter is a symbolic map name, indicating one of ten maps to set. The <i>mapsize</i> parameter specifies the number of entries in the map, and <i>values</i> is a pointer to an array of <i>mapsize</i> map values.

The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers. Maps that store color component values (all but GL_PIXEL_MAP_I_TO_I and GL_PIXEL_MAP_S_TO_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes. Floating-point values specified by <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMapfv</a> are converted directly to the internal floating-point format of these maps, and then clamped to the range [0,1]. Unsigned integer values specified by <b>glPixelMapusv</b> and <b>glPixelMapuiv</b> are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.

Maps that store indexes, GL_PIXEL_MAP_I_TO_I and GL_PIXEL_MAP_S_TO_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point. Floating-point values specified by <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMapfv</a> are converted directly to the internal fixed-point format of these maps. Unsigned integer values specified by <b>glPixelMapusv</b> and <b>glPixelMapuiv</b> specify integer values, with all zeros to the right of the binary point.

The following table shows the initial sizes and values for each of the maps. Maps that are indexed by either color or stencil indexes must have <i>mapsize</i> = 2 ^ <i>n</i> for some <i>n</i> or results are undefined. The maximum allowable size for each map depends on the implementation and can be determined by calling <b>glGet</b> with argument GL_MAX_PIXEL_MAP_TABLE. The single maximum applies to all maps, and it is at least 32.

<table>
<tr>
<th>Map</th>
<th>Lookup Index</th>
<th>Lookup Value</th>
<th>Initial Size</th>
<th>Initial Value</th>
</tr>
<tr>
<td>GL_PIXEL_MAP_I_TO_I</td>
<td>color index</td>
<td>color index</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_S_TO_S</td>
<td>stencil index</td>
<td>stencil index</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_I_TO_R</td>
<td>color index</td>
<td>R</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_I_TO_G</td>
<td>color index</td>
<td>G</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_I_TO_B</td>
<td>color index</td>
<td>B</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_I_TO_A</td>
<td>color index</td>
<td>A</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_R_TO_R</td>
<td>R</td>
<td>R</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_G_TO_G</td>
<td>G</td>
<td>G</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_B_TO_B</td>
<td>B</td>
<td>B</td>
<td>1</td>
<td>0.0</td>
</tr>
<tr>
<td>GL_PIXEL_MAP_A_TO_A</td>
<td>A</td>
<td>A</td>
<td>1</td>
<td>0.0</td>
</tr>
</table>
 

The following functions retrieve information related to <b>glPixelMap</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_PIXEL_MAP_I_TO_I_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_S_TO_S_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_I_TO_R_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_I_TO_G_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_I_TO_B_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_I_TO_A_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_R_TO_R_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_G_TO_G_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_B_TO_B_SIZE

<b>glGet</b> with argument GL_PIXEL_MAP_A_TO_A_SIZE

<b>glGet</b> with argument GL_MAX_PIXEL_MAP_TABLE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>
 

 

