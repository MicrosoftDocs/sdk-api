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

Specifies that mesh and amplification shaders are not supported.

### -field D3D12_SAMPLER_FEEDBACK_TIER_0_9:90

Specifies that mesh and amplification shaders are supported to tier 0.9.

### -field D3D12_SAMPLER_FEEDBACK_TIER_1_0:100

Specifies that mesh and amplification shaders are supported to tier 1.0.

### -field D3D12_MESH_SHADER_TIER_NOT_SUPPORTED:0

## -remarks

## -see-also

* [Sampler feedback spec](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)
