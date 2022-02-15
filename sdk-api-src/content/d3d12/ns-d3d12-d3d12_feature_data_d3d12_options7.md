---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS7
title: D3D12_FEATURE_DATA_D3D12_OPTIONS7
description: Indicates the level of support that the adapter provides for mesh and amplification shaders, and for sampler feedback.
tech.root: direct3d12
ms.date: 07/21/2021
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS7
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS7
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS7
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS7
---

## -description

Indicates the level of support that the adapter provides for mesh and amplification shaders, and for sampler feedback.

## -struct-fields

### -field MeshShaderTier

Type: \_Out\_ **[D3D12_MESH_SHADER_TIER](ne-d3d12-d3d12_mesh_shader_tier.md)**

Indicates the level of support for mesh and amplification shaders.

### -field SamplerFeedbackTier

Type: \_Out\_ **[D3D12_SAMPLER_FEEDBACK_TIER](ne-d3d12-d3d12_sampler_feedback_tier.md)**

Indicates the level of support for sampler feedback.

## -remarks

## -see-also

* [Mesh shader spec](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)
* [Sampler feedback spec](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)
