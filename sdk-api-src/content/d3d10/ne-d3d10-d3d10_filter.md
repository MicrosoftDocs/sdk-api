---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D3D10_FILTER enumeration


## -description


Filtering options during texture sampling.


## -enum-fields




### -field D3D10_FILTER_MIN_MAG_MIP_POINT

Use point sampling for minification, magnification, and mip-level sampling.


### -field D3D10_FILTER_MIN_MAG_POINT_MIP_LINEAR

Use point sampling for minification and magnification; use linear interpolation for mip-level sampling.


### -field D3D10_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT

Use point sampling for minification; use linear interpolation for magnification; use point sampling for mip-level sampling.


### -field D3D10_FILTER_MIN_POINT_MAG_MIP_LINEAR

Use point sampling for minification; use linear interpolation for magnification and mip-level sampling.


### -field D3D10_FILTER_MIN_LINEAR_MAG_MIP_POINT

Use linear interpolation for minification; use point sampling for magnification and mip-level sampling.


### -field D3D10_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR

Use linear interpolation for minification; use point sampling for magnification; use linear interpolation for mip-level sampling.


### -field D3D10_FILTER_MIN_MAG_LINEAR_MIP_POINT

Use linear interpolation for minification and magnification; use point sampling for mip-level sampling.


### -field D3D10_FILTER_MIN_MAG_MIP_LINEAR

Use linear interpolation for minification, magnification, and mip-level sampling.


### -field D3D10_FILTER_ANISOTROPIC

Use anisotropic interpolation for minification, magnification, and mip-level sampling.


### -field D3D10_FILTER_COMPARISON_MIN_MAG_MIP_POINT

Use point sampling for minification, magnification, and mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_COMPARISON_MIN_MAG_POINT_MIP_LINEAR

Use point sampling for minification and magnification; use linear interpolation for mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_COMPARISON_MIN_POINT_MAG_LINEAR_MIP_POINT

Use point sampling for minification; use linear interpolation for magnification; use point sampling for mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_COMPARISON_MIN_POINT_MAG_MIP_LINEAR

Use point sampling for minification; use linear interpolation for magnification and mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_COMPARISON_MIN_LINEAR_MAG_MIP_POINT

Use linear interpolation for minification; use point sampling for magnification and mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_COMPARISON_MIN_LINEAR_MAG_POINT_MIP_LINEAR

Use linear interpolation for minification; use point sampling for magnification; use linear interpolation for mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_COMPARISON_MIN_MAG_LINEAR_MIP_POINT

Use linear interpolation for minification and magnification; use point sampling for mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_COMPARISON_MIN_MAG_MIP_LINEAR

Use linear interpolation for minification, magnification, and mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_COMPARISON_ANISOTROPIC

Use anisotropic interpolation for minification, magnification, and mip-level sampling. Compare the result to the comparison value.


### -field D3D10_FILTER_TEXT_1BIT

For use in pixel shaders with textures that have the R1_UNORM format.


## -remarks



During texture sampling, one or more texels are read and combined (this is calling filtering) to produce a single value. Point sampling reads a single texel while linear sampling reads two texels (endpoints) and linearly interpolates a third value between the endpoints.

HLSL texture-sampling functions also support comparison filtering during texture sampling. Comparison filtering compares each sampled texel against a comparison value. The boolean result is blended the same way that normal texture filtering is blended.

You can use HLSL intrinsic texture-sampling functions that implement texture filtering only or companion functions that use texture filtering with comparison filtering.

<table>
<tr>
<th>Texture Sampling Function</th>
<th>Texture Sampling Function with Comparison Filtering</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/788ba4b4-8013-411f-9a19-fb9983386fa0">sample</a>
</td>
<td>
<a href="https://msdn.microsoft.com/e21894c4-e8c5-4c3d-92c1-727964f8fd94">samplecmp</a> or <a href="https://msdn.microsoft.com/cecfc5e8-d293-4e0e-a3f4-b23f84843b7d">samplecmplevelzero</a>
</td>
</tr>
</table>
 

Comparison filters only work with textures that have the following <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">formats</a>: R32_FLOAT_X8X24_TYPELESS, R32_FLOAT, R24_UNORM_X8_TYPELESS, R16_UNORM.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>
 

 

