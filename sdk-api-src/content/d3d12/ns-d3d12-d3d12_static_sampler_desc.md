---
UID: NS:d3d12.D3D12_STATIC_SAMPLER_DESC
title: D3D12_STATIC_SAMPLER_DESC (d3d12.h)
description: Describes a static sampler.
helpviewer_keywords: ["D3D12_STATIC_SAMPLER_DESC","D3D12_STATIC_SAMPLER_DESC structure","d3d12/D3D12_STATIC_SAMPLER_DESC","direct3d12.d3d12_static_sampler_desc"]
old-location: direct3d12\d3d12_static_sampler_desc.htm
tech.root: direct3d12
ms.assetid: 35553C1C-3661-4778-8BC5-F2E6775DF96D
ms.date: 12/05/2018
ms.keywords: D3D12_STATIC_SAMPLER_DESC, D3D12_STATIC_SAMPLER_DESC structure, d3d12/D3D12_STATIC_SAMPLER_DESC, direct3d12.d3d12_static_sampler_desc
req.header: d3d12.h
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
req.typenames: D3D12_STATIC_SAMPLER_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_STATIC_SAMPLER_DESC
 - d3d12/D3D12_STATIC_SAMPLER_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_STATIC_SAMPLER_DESC
---

# D3D12_STATIC_SAMPLER_DESC structure


## -description

Describes a static sampler.

## -struct-fields

### -field Filter

The filtering method to use when sampling a texture, as a <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter">D3D12_FILTER</a> enumeration constant.

### -field AddressU

Specifies the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode">D3D12_TEXTURE_ADDRESS_MODE</a> mode to use for resolving a <i>u</i> texture coordinate that is outside the 0 to 1 range.

### -field AddressV

Specifies the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode">D3D12_TEXTURE_ADDRESS_MODE</a> mode to use for resolving a <i>v</i> texture coordinate that is outside the 0 to 1 range.

### -field AddressW

Specifies the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode">D3D12_TEXTURE_ADDRESS_MODE</a> mode to use for resolving a <i>w</i> texture coordinate that is outside the 0 to 1 range.

### -field MipLODBias

Offset from the calculated mipmap level. For example, if Direct3D calculates that a texture should be sampled at mipmap level 3 and MipLODBias is 2, then the texture will be sampled at mipmap level 5.

### -field MaxAnisotropy

Clamping value used if D3D12_FILTER_ANISOTROPIC or D3D12_FILTER_COMPARISON_ANISOTROPIC is specified as the filter. Valid values are between 1 and 16.

### -field ComparisonFunc

A function that compares sampled data against existing sampled data. 
            The function options are listed in <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func">D3D12_COMPARISON_FUNC</a>.

### -field BorderColor

One member of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color">D3D12_STATIC_BORDER_COLOR</a>, the border color to use if D3D12_TEXTURE_ADDRESS_MODE_BORDER is specified for AddressU, AddressV, or AddressW. 
            Range must be between 0.0 and 1.0 inclusive.

### -field MinLOD

Lower end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed.

### -field MaxLOD

Upper end of the mipmap range to clamp access to, where 0 is the largest and most detailed mipmap level and any level higher than that is less detailed. This value must be greater than or equal to MinLOD. To have no upper limit on LOD set this to a large value such as D3D12_FLOAT32_MAX.

### -field ShaderRegister

The <i>ShaderRegister</i> and <i>RegisterSpace</i> parameters correspond to the binding syntax of HLSL.  For example, in HLSL:
            


``` syntax
Texture2D<float4> a : register(t2, space3);
```

This corresponds to a  <i>ShaderRegister</i> of 2 (indicating the type is SRV), and <i>RegisterSpace</i> is 3.
            

The  <i>ShaderRegister</i> and <i>RegisterSpace</i> pair is needed to establish correspondence between shader resources and runtime heap descriptors, using the root signature data structure.

### -field RegisterSpace

See the description for <i>ShaderRegister</i>.
            Register space is optional; the default register space is 0.

### -field ShaderVisibility

Specifies the visibility of the sampler to the pipeline shaders, one member of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility">D3D12_SHADER_VISIBILITY</a>.

## -remarks

Use this structure with the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-static-sampler-desc">CD3DX12_STATIC_SAMPLER_DESC</a>



<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
