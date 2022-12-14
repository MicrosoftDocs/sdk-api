---
UID: NE:d3d12sdklayers.D3D12_GPU_BASED_VALIDATION_FLAGS
title: D3D12_GPU_BASED_VALIDATION_FLAGS (d3d12sdklayers.h)
description: Describes the level of GPU-based validation to perform at runtime.
helpviewer_keywords: ["D3D12_GPU_BASED_VALIDATION_FLAGS","D3D12_GPU_BASED_VALIDATION_FLAGS enumeration","D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING","D3D12_GPU_BASED_VALIDATION_FLAGS_NONE","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING","d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS_NONE","direct3d12.d3d12_gpu_based_validation_flags"]
old-location: direct3d12\d3d12_gpu_based_validation_flags.htm
tech.root: direct3d12
ms.assetid: D9FA7F77-8DE8-4630-A9C7-E95B9E997E23
ms.date: 12/05/2018
ms.keywords: D3D12_GPU_BASED_VALIDATION_FLAGS, D3D12_GPU_BASED_VALIDATION_FLAGS enumeration, D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING, D3D12_GPU_BASED_VALIDATION_FLAGS_NONE, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS_NONE, direct3d12.d3d12_gpu_based_validation_flags
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
req.typenames: D3D12_GPU_BASED_VALIDATION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_GPU_BASED_VALIDATION_FLAGS
 - d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS
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
 - D3D12_GPU_BASED_VALIDATION_FLAGS
---

# D3D12_GPU_BASED_VALIDATION_FLAGS enumeration


## -description

Describes the level of GPU-based validation to perform at runtime.

## -enum-fields

### -field D3D12_GPU_BASED_VALIDATION_FLAGS_NONE:0

Default behavior; resource states, descriptors, and descriptor tables are all validated.

### -field D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING:0x1

When set, GPU-based validation does not perform resource state validation which greatly reduces the performance cost of GPU-based validation. Descriptors and descriptor heaps are still validated.

## -remarks

This enumeration is used with the <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug2-setgpubasedvalidationflags">ID3D12Debug2::SetGPUBasedValidationFlags</a> method to configure the amount of runtime validation that will occur.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
