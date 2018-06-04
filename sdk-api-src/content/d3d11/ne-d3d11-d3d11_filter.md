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

# D3D11_FILTER enumeration


## -description


Filtering options during texture sampling.


## -enum-fields




### -field D3D11_FILTER_MIN_MAG_MIP_POINT

Use point sampling for minification, magnification, and mip-level sampling.


### -field D3D11_FILTER_MIN_MAG_POINT_MIP_LINEAR

Use point sampling for minification and magnification; use linear interpolation for mip-level sampling.


### -field D3D11_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT

Use point sampling for minification; use linear interpolation for magnification; use point sampling for mip-level sampling.


### -field D3D11_FILTER_MIN_POINT_MAG_MIP_LINEAR

Use point sampling for minification; use linear interpolation for magnification and mip-level sampling.


### -field D3D11_FILTER_MIN_LINEAR_MAG_MIP_POINT

Use linear interpolation for minification; use point sampling for magnification and mip-level sampling.


### -field D3D11_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR

Use linear interpolation for minification; use point sampling for magnification; use linear interpolation for mip-level sampling.


### -field D3D11_FILTER_MIN_MAG_LINEAR_MIP_POINT

Use linear interpolation for minification and magnification; use point sampling for mip-level sampling.


### -field D3D11_FILTER_MIN_MAG_MIP_LINEAR

Use linear interpolation for minification, magnification, and mip-level sampling.


### -field D3D11_FILTER_ANISOTROPIC

Use anisotropic interpolation for minification, magnification, and mip-level sampling.


### -field D3D11_FILTER_COMPARISON_MIN_MAG_MIP_POINT

Use point sampling for minification, magnification, and mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_COMPARISON_MIN_MAG_POINT_MIP_LINEAR

Use point sampling for minification and magnification; use linear interpolation for mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_COMPARISON_MIN_POINT_MAG_LINEAR_MIP_POINT

Use point sampling for minification; use linear interpolation for magnification; use point sampling for mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_COMPARISON_MIN_POINT_MAG_MIP_LINEAR

Use point sampling for minification; use linear interpolation for magnification and mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_COMPARISON_MIN_LINEAR_MAG_MIP_POINT

Use linear interpolation for minification; use point sampling for magnification and mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_COMPARISON_MIN_LINEAR_MAG_POINT_MIP_LINEAR

Use linear interpolation for minification; use point sampling for magnification; use linear interpolation for mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_COMPARISON_MIN_MAG_LINEAR_MIP_POINT

Use linear interpolation for minification and magnification; use point sampling for mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_COMPARISON_MIN_MAG_MIP_LINEAR

Use linear interpolation for minification, magnification, and mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_COMPARISON_ANISOTROPIC

Use anisotropic interpolation for minification, magnification, and mip-level sampling. Compare the result to the comparison value.


### -field D3D11_FILTER_MINIMUM_MIN_MAG_MIP_POINT

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_MAG_MIP_POINT</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MINIMUM_MIN_MAG_POINT_MIP_LINEAR

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_MAG_POINT_MIP_LINEAR</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MINIMUM_MIN_POINT_MAG_LINEAR_MIP_POINT

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MINIMUM_MIN_POINT_MAG_MIP_LINEAR

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_POINT_MAG_MIP_LINEAR</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MINIMUM_MIN_LINEAR_MAG_MIP_POINT

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_LINEAR_MAG_MIP_POINT</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MINIMUM_MIN_LINEAR_MAG_POINT_MIP_LINEAR

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MINIMUM_MIN_MAG_LINEAR_MIP_POINT

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_MAG_LINEAR_MIP_POINT</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MINIMUM_MIN_MAG_MIP_LINEAR

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_MAG_MIP_LINEAR</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MINIMUM_ANISOTROPIC

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_ANISOTROPIC</a> and instead of filtering them return the minimum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the minimum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_MIN_MAG_MIP_POINT

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_MAG_MIP_POINT</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_MIN_MAG_POINT_MIP_LINEAR

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_MAG_POINT_MIP_LINEAR</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_MIN_POINT_MAG_LINEAR_MIP_POINT

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_POINT_MAG_LINEAR_MIP_POINT</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_MIN_POINT_MAG_MIP_LINEAR

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_POINT_MAG_MIP_LINEAR</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_MIN_LINEAR_MAG_MIP_POINT

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_LINEAR_MAG_MIP_POINT</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_MIN_LINEAR_MAG_POINT_MIP_LINEAR

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_LINEAR_MAG_POINT_MIP_LINEAR</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_MIN_MAG_LINEAR_MIP_POINT

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_MAG_LINEAR_MIP_POINT</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_MIN_MAG_MIP_LINEAR

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_MIN_MAG_MIP_LINEAR</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


### -field D3D11_FILTER_MAXIMUM_ANISOTROPIC

Fetch the same set of texels as <a href="https://docs.microsoft.com/">D3D11_FILTER_ANISOTROPIC</a> and instead of filtering them return the maximum of the texels.  Texels that are weighted 0 during filtering aren't counted towards the maximum.  You can query support for this filter type from the <b>MinMaxFiltering</b> member in the <a href="https://msdn.microsoft.com/940381BB-E8E6-416D-8F36-CC3591E70702">D3D11_FEATURE_DATA_D3D11_OPTIONS1</a> structure.


## -remarks



<div class="alert"><b>Note</b>  If you use different filter types for min versus mag filter, undefined behavior occurs in certain cases where the choice between whether magnification or minification happens is ambiguous.  To prevent this undefined behavior, use filter modes that use similar filter operations for both min and mag (or use anisotropic filtering, which avoids the issue as well).</div>
<div> </div>
During texture sampling, one or more texels are read and combined (this is calling filtering) to produce a single value. Point sampling reads a single texel while linear sampling reads two texels (endpoints) and linearly interpolates a third value between the endpoints.

HLSL texture-sampling functions also support comparison filtering during texture sampling. Comparison filtering compares each sampled texel against a comparison value. The boolean result is blended the same way that normal texture filtering is blended.

You can use HLSL intrinsic texture-sampling functions that implement texture filtering only or companion functions that use texture filtering with comparison filtering.

<table>
<tr>
<th>Texture Sampling Function</th>
<th>Texture Sampling Function with Comparison Filtering</th>
</tr>
<tr>
<td>sample</td>
<td>samplecmp or samplecmplevelzero</td>
</tr>
</table>
 

Comparison filters only work with textures that have the following DXGI formats: R32_FLOAT_X8X24_TYPELESS, R32_FLOAT, R24_UNORM_X8_TYPELESS, R16_UNORM.




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

