---
UID: NS:d3d11.D3D11_SAMPLER_DESC
title: D3D11_SAMPLER_DESC
author: windows-sdk-content
description: Describes a sampler state.
old-location: direct3d11\d3d11_sampler_desc.htm
tech.root: direct3d11
ms.assetid: 97dd6cac-6657-4a1e-b631-4e5d36994b16
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_SAMPLER_DESC, D3D11_SAMPLER_DESC structure [Direct3D 11], bb0f20c3-8e57-c2fb-f34c-640d23b254ab, d3d11/D3D11_SAMPLER_DESC, direct3d11.d3d11_sampler_desc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d11.h
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
 - D3D11.h
api_name:
 - D3D11_SAMPLER_DESC
product: Windows
targetos: Windows
req.typenames: D3D11_SAMPLER_DESC
req.redist: 
---

# D3D11_SAMPLER_DESC structure


## -description


Describes a sampler state.


## -struct-fields




### -field Filter

Type: <b><a href="https://msdn.microsoft.com/873b7910-4686-4f0c-a674-2aa3585a9b36">D3D11_FILTER</a></b>

Filtering method to use when sampling a texture (see <a href="https://msdn.microsoft.com/873b7910-4686-4f0c-a674-2aa3585a9b36">D3D11_FILTER</a>).
          


### -field AddressU

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476256(v=VS.85).aspx">D3D11_TEXTURE_ADDRESS_MODE</a></b>

Method to use for resolving a u texture coordinate that is outside the 0 to 1 range (see <a href="https://msdn.microsoft.com/en-us/library/Ff476256(v=VS.85).aspx">D3D11_TEXTURE_ADDRESS_MODE</a>).
          


### -field AddressV

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476256(v=VS.85).aspx">D3D11_TEXTURE_ADDRESS_MODE</a></b>

Method to use for resolving a v texture coordinate that is outside the 0 to 1 range.


### -field AddressW

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476256(v=VS.85).aspx">D3D11_TEXTURE_ADDRESS_MODE</a></b>

Method to use for resolving a w texture coordinate that is outside the 0 to 1 range.


### -field MipLODBias

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">FLOAT</a></b>

Offset from the calculated mipmap level. For example, if Direct3D calculates that a texture should be sampled at mipmap level 3 and MipLODBias is 2, then the texture will be sampled at mipmap level 5.


### -field MaxAnisotropy

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Clamping value used if D3D11_FILTER_ANISOTROPIC or D3D11_FILTER_COMPARISON_ANISOTROPIC is specified in Filter. Valid values are between 1 and 16.


### -field ComparisonFunc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476101(v=VS.85).aspx">D3D11_COMPARISON_FUNC</a></b>

A function that compares sampled data against existing sampled data. The function options are listed in <a href="https://msdn.microsoft.com/en-us/library/Ff476101(v=VS.85).aspx">D3D11_COMPARISON_FUNC</a>.
          


### -field BorderColor

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">FLOAT</a>[4]</b>

Border color to use if D3D11_TEXTURE_ADDRESS_BORDER is specified for AddressU, AddressV, or AddressW. Range must be between 0.0 and 1.0 inclusive.


### -field MinLOD

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">FLOAT</a></b>

Lower end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed.


### -field MaxLOD

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">FLOAT</a></b>

Upper end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed. This value must be greater than or equal to MinLOD. To have no upper limit on LOD set this to a large value such as D3D11_FLOAT32_MAX.


## -remarks



These are the default values for sampler state.

<table>
<tr>
<th>State</th>
<th>Default Value</th>
</tr>
<tr>
<td>Filter</td>
<td>D3D11_FILTER_MIN_MAG_MIP_LINEAR</td>
</tr>
<tr>
<td>AddressU</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>AddressV</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>AddressW</td>
<td>D3D11_TEXTURE_ADDRESS_CLAMP</td>
</tr>
<tr>
<td>MinLOD</td>
<td>-3.402823466e+38F (-FLT_MAX)</td>
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
<td>1</td>
</tr>
<tr>
<td>ComparisonFunc</td>
<td>D3D11_COMPARISON_NEVER</td>
</tr>
<tr>
<td>BorderColor</td>
<td>float4(1.0f,1.0f,1.0f,1.0f)</td>
</tr>
<tr>
<td>Texture</td>
<td>N/A</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476155(v=VS.85).aspx">Core Structures</a>
 

 

