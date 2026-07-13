---
UID: NF:d3d12sdklayers.ID3D12Debug3.SetGPUBasedValidationFlags
title: ID3D12Debug3::SetGPUBasedValidationFlags (d3d12sdklayers.h)
description: This method configures the level of GPU-based validation that the debug device is to perform at runtime. (ID3D12Debug3.SetGPUBasedValidationFlags)
helpviewer_keywords: ["- ID3D12Debug3.SetGPUBasedValidationFlags"]
tech.root: direct3d12
ms.date: 03/02/2020
req.header: d3d12sdklayers.h
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
req.typenames: 
req.redist: 
f1_keywords:
 - ID3D12Debug3::SetGPUBasedValidationFlags
 - d3d12sdklayers/ID3D12Debug3::SetGPUBasedValidationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug3.SetGPUBasedValidationFlags
---

## -description

This method configures the level of GPU-based validation that the debug device is to perform at runtime.

## -parameters

### -param Flags

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags">D3D12_GPU_BASED_VALIDATION_FLAGS</a></b>

Specifies the level of GPU-based validation to perform at runtime.

## -remarks

This method overrides the default behavior of GPU-based validation so it must be called before creating the D3D12 Device. These settings can't be changed or cancelled after the device is created. If you want to change the behavior of GPU-based validation at a later time, the device must be destroyed and recreated with different parameters.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug3">ID3D12Debug3</a>
