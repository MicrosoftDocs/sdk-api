---
UID: NE:d3d12.D3D12_SAMPLER_FEEDBACK_TIER
title: D3D12_SAMPLER_FEEDBACK_TIER
description: Defines constants that specify sampler feedback support.
ms.date: 07/21/2021
tech.root: direct3d12
req.construct-type: enumeration
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.redist: 
f1_keywords:
 - D3D12_SAMPLER_FEEDBACK_TIER
 - d3d12/D3D12_SAMPLER_FEEDBACK_TIER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_SAMPLER_FEEDBACK_TIER
---

## -description

Defines constants that specify sampler feedback support.

## -enum-fields

### -field D3D12_SAMPLER_FEEDBACK_TIER_NOT_SUPPORTED:0

Specifies that sampler feedback is not supported. Attempts at calling sampler feedback APIs represent an error.

### -field D3D12_SAMPLER_FEEDBACK_TIER_0_9:90

Specifies that sampler feedback is supported to tier 0.9. This indicates the following:

Sampler feedback is supported for samplers with these texture addressing modes:
* D3D12_TEXTURE_ADDRESS_MODE_WRAP
* D3D12_TEXTURE_ADDRESS_MODE_CLAMP

The Texture2D shader resource view passed in to feedback-writing HLSL methods has these restrictions:
* The MostDetailedMip field must be 0.
* The MipLevels count must span the full mip count of the resource.
* The PlaneSlice field must be 0.
* The ResourceMinLODClamp field must be 0.

The Texture2DArray shader resource view passed in to feedback-writing HLSL methods has these restrictions:
* All the limitations as in Texture2D above, and
* The FirstArraySlice field must be 0.
* The ArraySize field must span the full array element count of the resource.

### -field D3D12_SAMPLER_FEEDBACK_TIER_1_0:100

Specifies sample feedback is supported to tier 1.0. This indicates that sampler feedback is supported for all texture addressing modes, and feedback-writing methods are supported irrespective of the passed-in shader resource view.

### -field D3D12_MESH_SHADER_TIER_NOT_SUPPORTED:0

## -remarks

## -see-also

* [Sampler feedback spec](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)
