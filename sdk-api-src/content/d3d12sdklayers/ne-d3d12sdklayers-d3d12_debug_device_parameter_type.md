---
UID: NE:d3d12sdklayers.D3D12_DEBUG_DEVICE_PARAMETER_TYPE
title: D3D12_DEBUG_DEVICE_PARAMETER_TYPE (d3d12sdklayers.h)
description: Specifies the data type of the memory pointed to by the pData parameter of ID3D12DebugDevice1::SetDebugParameter and ID3D12DebugDevice1::GetDebugParameter.
helpviewer_keywords: ["D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS","D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS","D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR","D3D12_DEBUG_DEVICE_PARAMETER_TYPE","D3D12_DEBUG_DEVICE_PARAMETER_TYPE enumeration","d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS","d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS","d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR","d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_TYPE","direct3d12.d3d12_debug_device_parameter_type"]
old-location: direct3d12\d3d12_debug_device_parameter_type.htm
tech.root: direct3d12
ms.assetid: 477155FF-9DF7-4E21-AF52-21EB3DBC3550
ms.date: 12/05/2018
ms.keywords: D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS, D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS, D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR, D3D12_DEBUG_DEVICE_PARAMETER_TYPE, D3D12_DEBUG_DEVICE_PARAMETER_TYPE enumeration, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_TYPE, direct3d12.d3d12_debug_device_parameter_type
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
req.typenames: D3D12_DEBUG_DEVICE_PARAMETER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEBUG_DEVICE_PARAMETER_TYPE
 - d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_TYPE
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
 - D3D12_DEBUG_DEVICE_PARAMETER_TYPE
---

# D3D12_DEBUG_DEVICE_PARAMETER_TYPE enumeration


## -description

Specifies the data type of the memory pointed to by the <i>pData</i> parameter of <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter">ID3D12DebugDevice1::SetDebugParameter</a> and <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter">ID3D12DebugDevice1::GetDebugParameter</a>.

## -enum-fields

### -field D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS:0

Indicates <i>pData</i> points to a <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature">D3D12_DEBUG_FEATURE</a> value.

### -field D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS

Indicates <i>pData</i> points to a <a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a> structure.

### -field D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR

Indicates <i>pData</i> points to a <a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor">D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-sdklayers-enumerations">Debug Layer Enumerations</a>



<a href="/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation">Using D3D12 Debug Layer GPU-Based Validation</a>
