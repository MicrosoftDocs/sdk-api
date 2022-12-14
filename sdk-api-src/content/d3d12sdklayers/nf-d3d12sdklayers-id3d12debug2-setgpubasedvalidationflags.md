---
UID: NF:d3d12sdklayers.ID3D12Debug2.SetGPUBasedValidationFlags
title: ID3D12Debug2::SetGPUBasedValidationFlags (d3d12sdklayers.h)
description: This method configures the level of GPU-based validation that the debug device is to perform at runtime. (ID3D12Debug2.SetGPUBasedValidationFlags)
helpviewer_keywords: ["ID3D12Debug2 interface","SetGPUBasedValidationFlags method","ID3D12Debug2.SetGPUBasedValidationFlags","ID3D12Debug2::SetGPUBasedValidationFlags","SetGPUBasedValidationFlags","SetGPUBasedValidationFlags method","SetGPUBasedValidationFlags method","ID3D12Debug2 interface","d3d12sdklayers/ID3D12Debug2::SetGPUBasedValidationFlags","direct3d12.id3d12debug2_setgpubasedvalidationflags"]
old-location: direct3d12\id3d12debug2_setgpubasedvalidationflags.htm
tech.root: direct3d12
ms.assetid: EA774CC4-7675-46AA-9CDF-56C8B9507702
ms.date: 12/05/2018
ms.keywords: ID3D12Debug2 interface,SetGPUBasedValidationFlags method, ID3D12Debug2.SetGPUBasedValidationFlags, ID3D12Debug2::SetGPUBasedValidationFlags, SetGPUBasedValidationFlags, SetGPUBasedValidationFlags method, SetGPUBasedValidationFlags method,ID3D12Debug2 interface, d3d12sdklayers/ID3D12Debug2::SetGPUBasedValidationFlags, direct3d12.id3d12debug2_setgpubasedvalidationflags
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Debug2::SetGPUBasedValidationFlags
 - d3d12sdklayers/ID3D12Debug2::SetGPUBasedValidationFlags
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
 - ID3D12Debug2.SetGPUBasedValidationFlags
---

## -description

This method configures the level of GPU-based validation that the debug device is to perform at runtime.

## -parameters

### -param Flags

Type: <b><a href="/windows/win32/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags">D3D12_GPU_BASED_VALIDATION_FLAGS</a></b>

Specifies the level of GPU-based validation to perform at runtime.

## -remarks

This method overrides the default behavior of GPU-based validation so it must be called before creating the Direct3D 12 device. These settings can't be changed or cancelled after the device is created. If you want to change the behavior of GPU-based validation at a later time, the device must be destroyed and recreated with different parameters.

## -see-also

<a href="/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug2">ID3D12Debug2</a>

