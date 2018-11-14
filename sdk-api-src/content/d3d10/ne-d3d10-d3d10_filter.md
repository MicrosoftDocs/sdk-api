---
UID: NE:d3d10.D3D10_FILTER
title: D3D10_FILTER
author: windows-sdk-content
description: Filtering options during texture sampling.
old-location: direct3d10\d3d10_filter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_filter.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 31eff5fe-8fd7-55df-9fc7-0567ce55ecd5, D3D10_FILTER, D3D10_FILTER enumeration [Direct3D 10], D3D10_FILTER_ANISOTROPIC, D3D10_FILTER_COMPARISON_ANISOTROPIC, D3D10_FILTER_COMPARISON_MIN_LINEAR_MAG_MIP_POINT, D3D10_FILTER_COMPARISON_MIN_LINEAR_MAG_POINT_MIP_LINEAR, D3D10_FILTER_COMPARISON_MIN_MAG_LINEAR_MIP_POINT, D3D10_FILTER_COMPARISON_MIN_MAG_MIP_LINEAR, D3D10_FILTER_COMPARISON_MIN_MAG_MIP_POINT, D3D10_FILTER_COMPARISON_MIN_MAG_POINT_MIP_LINEAR, D3D10_FILTER_COMPARISON_MIN_POINT_MAG_LINEAR_MIP_POINT, D3D10_FILTER_COMPARISON_MIN_POINT_MAG_MIP_LINEAR, D3D10_FILTER_MIN_LINEAR_MAG_MIP_POINT, D3D10_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR, D3D10_FILTER_MIN_MAG_LINEAR_MIP_POINT, D3D10_FILTER_MIN_MAG_MIP_LINEAR, D3D10_FILTER_MIN_MAG_MIP_POINT, D3D10_FILTER_MIN_MAG_POINT_MIP_LINEAR, D3D10_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT, D3D10_FILTER_MIN_POINT_MAG_MIP_LINEAR, D3D10_FILTER_TEXT_1BIT, d3d10/D3D10_FILTER, d3d10/D3D10_FILTER_ANISOTROPIC, d3d10/D3D10_FILTER_COMPARISON_ANISOTROPIC, d3d10/D3D10_FILTER_COMPARISON_MIN_LINEAR_MAG_MIP_POINT, d3d10/D3D10_FILTER_COMPARISON_MIN_LINEAR_MAG_POINT_MIP_LINEAR, d3d10/D3D10_FILTER_COMPARISON_MIN_MAG_LINEAR_MIP_POINT, d3d10/D3D10_FILTER_COMPARISON_MIN_MAG_MIP_LINEAR, d3d10/D3D10_FILTER_COMPARISON_MIN_MAG_MIP_POINT, d3d10/D3D10_FILTER_COMPARISON_MIN_MAG_POINT_MIP_LINEAR, d3d10/D3D10_FILTER_COMPARISON_MIN_POINT_MAG_LINEAR_MIP_POINT, d3d10/D3D10_FILTER_COMPARISON_MIN_POINT_MAG_MIP_LINEAR, d3d10/D3D10_FILTER_MIN_LINEAR_MAG_MIP_POINT, d3d10/D3D10_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR, d3d10/D3D10_FILTER_MIN_MAG_LINEAR_MIP_POINT, d3d10/D3D10_FILTER_MIN_MAG_MIP_LINEAR, d3d10/D3D10_FILTER_MIN_MAG_MIP_POINT, d3d10/D3D10_FILTER_MIN_MAG_POINT_MIP_LINEAR, d3d10/D3D10_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT, d3d10/D3D10_FILTER_MIN_POINT_MAG_MIP_LINEAR, d3d10/D3D10_FILTER_TEXT_1BIT, direct3d10.d3d10_filter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_FILTER
product: Windows
targetos: Windows
req.typenames: D3D10_FILTER
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Bb509695(v=VS.85).aspx">sample</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb509696(v=VS.85).aspx">samplecmp</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb509697(v=VS.85).aspx">samplecmplevelzero</a>
</td>
</tr>
</table>
 

Comparison filters only work with textures that have the following <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">formats</a>: R32_FLOAT_X8X24_TYPELESS, R32_FLOAT, R24_UNORM_X8_TYPELESS, R16_UNORM.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205150(v=VS.85).aspx">Core Enumerations</a>
 

 

