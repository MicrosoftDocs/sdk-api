---
UID: NS:d3d12sdklayers.D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
title: D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR (d3d12sdklayers.h)
description: Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.
helpviewer_keywords: ["D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR","D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR structure","d3d12sdklayers/D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR","direct3d12.d3d12_debug_device_gpu_slowdown_performance_factor"]
old-location: direct3d12\d3d12_debug_device_gpu_slowdown_performance_factor.htm
tech.root: direct3d12
ms.assetid: C137DFAA-7AB9-49A6-882D-61ADE6E9E046
ms.date: 12/05/2018
ms.keywords: D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR, D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR structure, d3d12sdklayers/D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR, direct3d12.d3d12_debug_device_gpu_slowdown_performance_factor
req.header: d3d12sdklayers.h
req.include-header: D3D12.h
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
req.typenames: D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
 - d3d12sdklayers/D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
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
 - D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR
---

# D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR structure


## -description

Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.

## -struct-fields

### -field SlowdownFactor

Specifies the amount of slowdown artificially applied, as a factor of the nominal time for the fence to signal. The default value is 0.

## -remarks

The SlowdownFactor is applied by artificially delaying the time it takes for a fence to signal. When SlowdownFactor is non-zero, the time taken for a fence to signal is approximately 1.0 + SlowdownFactor times the length of the nominal timing.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>