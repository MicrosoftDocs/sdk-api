---
UID: NS:d3d10.D3D10_SAMPLER_DESC
title: D3D10_SAMPLER_DESC (d3d10.h)
description: Describes a sampler state. (D3D10_SAMPLER_DESC)
helpviewer_keywords: ["3a645765-f6d2-d3f9-5cfb-b48ca43f620b","D3D10_SAMPLER_DESC","D3D10_SAMPLER_DESC structure [Direct3D 10]","d3d10/D3D10_SAMPLER_DESC","direct3d10.d3d10_sampler_desc"]
old-location: direct3d10\d3d10_sampler_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_sampler_desc.htm
ms.date: 12/05/2018
ms.keywords: 3a645765-f6d2-d3f9-5cfb-b48ca43f620b, D3D10_SAMPLER_DESC, D3D10_SAMPLER_DESC structure [Direct3D 10], d3d10/D3D10_SAMPLER_DESC, direct3d10.d3d10_sampler_desc
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
targetos: Windows
req.typenames: D3D10_SAMPLER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_SAMPLER_DESC
 - d3d10/D3D10_SAMPLER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_SAMPLER_DESC
---

# D3D10_SAMPLER_DESC structure


## -description

Describes a sampler state.

## -struct-fields

### -field Filter

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_filter">D3D10_FILTER</a></b>

Filtering method to use when sampling a texture (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_filter">D3D10_FILTER</a>).

### -field AddressU

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_texture_address_mode">D3D10_TEXTURE_ADDRESS_MODE</a></b>

Method to use for resolving a u texture coordinate that is outside the 0 to 1 range (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_texture_address_mode">D3D10_TEXTURE_ADDRESS_MODE</a>).

### -field AddressV

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_texture_address_mode">D3D10_TEXTURE_ADDRESS_MODE</a></b>

Method to use for resolving a v texture coordinate that is outside the 0 to 1 range.

### -field AddressW

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_texture_address_mode">D3D10_TEXTURE_ADDRESS_MODE</a></b>

Method to use for resolving a w texture coordinate that is outside the 0 to 1 range.

### -field MipLODBias

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Offset from the calculated mipmap level. For example, if Direct3D calculates that a texture should be sampled at mipmap level 3 and MipLODBias is 2, then the texture will be sampled at mipmap level 5.

### -field MaxAnisotropy

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Clamping value used if D3D10_FILTER_ANISOTROPIC or D3D10_FILTER_COMPARISON_ANISOTROPIC is specified in Filter. Valid values are between 1 and 16.

### -field ComparisonFunc

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_comparison_func">D3D10_COMPARISON_FUNC</a></b>

A function that compares sampled data against existing sampled data. The function options are listed in <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_comparison_func">D3D10_COMPARISON_FUNC</a>.

### -field BorderColor

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Border color to use if D3D10_TEXTURE_ADDRESS_BORDER is specified for AddressU, AddressV, or AddressW. Range must be between 0.0 and 1.0 inclusive.

### -field MinLOD

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Lower end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed.

### -field MaxLOD

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Upper end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed. This value must be greater than or equal to MinLOD. To have no upper limit on LOD set this to a large value such as D3D10_FLOAT32_MAX.

## -remarks

These are the default values for sampler state.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>Filter</td>
<td>Min_Mag_Mip_Point</td>
</tr>
<tr>
<td>AddressU</td>
<td>Clamp</td>
</tr>
<tr>
<td>AddressV</td>
<td>Clamp</td>
</tr>
<tr>
<td>AddressW</td>
<td>Clamp</td>
</tr>
<tr>
<td>MinLOD</td>
<td>0.0f</td>
</tr>
<tr>
<td>MaxLOD</td>
<td>3.402823466e+38F (FLT_MAX)</td>
</tr>
<tr>
<td>MipMapLODBias</td>
<td>0.0f</td>
</tr>
<tr>
<td>MaxAnisotropy</td>
<td>16</td>
</tr>
<tr>
<td>ComparisonFunc</td>
<td>Never</td>
</tr>
<tr>
<td>BorderColor</td>
<td>float4(0.0f, 0.0f, 0.0f, 0.0f)</td>
</tr>
<tr>
<td>Texture</td>
<td>N/A</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
