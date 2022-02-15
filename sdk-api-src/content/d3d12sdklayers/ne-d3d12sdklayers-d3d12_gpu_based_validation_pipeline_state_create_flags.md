---
UID: NE:d3d12sdklayers.D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS
title: D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS (d3d12sdklayers.h)
description: Specifies how GPU-Based Validation handles patched pipeline states during ID3D12Device::CreateGraphicsPipelineState and ID3D12Device::CreateComputePipelineState.
helpviewer_keywords: ["D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS","D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS enumeration","D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS_VALID_MASK","D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_GUARDED_VALIDATION_SHADERS","D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_TRACKING_ONLY_SHADERS","D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_UNGUARDED_VALIDATION_SHADERS","D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_NONE","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS_VALID_MASK","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_GUARDED_VALIDATION_SHADERS","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_TRACKING_ONLY_SHADERS","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_UNGUARDED_VALIDATION_SHADERS","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_NONE","direct3d12.d3d12_gpu_based_validation_pipeline_state_create_flags"]
old-location: direct3d12\d3d12_gpu_based_validation_pipeline_state_create_flags.htm
tech.root: direct3d12
ms.assetid: B3D0ABD0-E7CE-4853-AC7C-228398B4588C
ms.date: 12/05/2018
ms.keywords: D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS, D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS enumeration, D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS_VALID_MASK, D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_GUARDED_VALIDATION_SHADERS, D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_TRACKING_ONLY_SHADERS, D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_UNGUARDED_VALIDATION_SHADERS, D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_NONE, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS_VALID_MASK, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_GUARDED_VALIDATION_SHADERS, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_TRACKING_ONLY_SHADERS, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_UNGUARDED_VALIDATION_SHADERS, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_NONE, direct3d12.d3d12_gpu_based_validation_pipeline_state_create_flags
req.header: d3d12sdklayers.h
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
req.typenames: D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS
 - d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS
---

# D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS enumeration


## -description

Specifies how GPU-Based Validation handles patched pipeline states during <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate">ID3D12Device::CreateGraphicsPipelineState</a> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate">ID3D12Device::CreateComputePipelineState</a>.

## -enum-fields

### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_NONE:0

This is the default value.  Indicates no patching of pipeline states should be done during PSO creation.  Instead PSO’s are patched on first use in a command list.  This can help to reduce the up-front cost of PSO creation but may instead slow down command list recording until a steady-state is reached.

### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_TRACKING_ONLY_SHADERS:0x1

Indicates that state-tracking GPU-Based Validation PSO’s should be created along with the original PSO at create time.

### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_UNGUARDED_VALIDATION_SHADERS:0x2

Indicates that unguarded GPU-Based Validation PSO’s should be created along with the original PSO at create time.

### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_GUARDED_VALIDATION_SHADERS:0x4

Indicates that guarded GPU-Based Validation PSO’s should be created along with the original PSO at create time.

### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS_VALID_MASK:0x7

Internal use only.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a> structure.

Generally speaking most application developers are likely to leave this parameter unchanged.  However, if the overhead of deferring patched PSO creation is suspected to be too much of a performance problem, then developers should consider changing this setting.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-sdklayers-enumerations">Debug Layer Enumerations</a>



<a href="/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation">Using D3D12 Debug Layer GPU-Based Validation</a>
