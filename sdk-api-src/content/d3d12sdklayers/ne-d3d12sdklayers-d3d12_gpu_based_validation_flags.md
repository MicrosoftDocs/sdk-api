---
UID: NE:d3d12sdklayers.D3D12_GPU_BASED_VALIDATION_FLAGS
title: D3D12_GPU_BASED_VALIDATION_FLAGS
author: windows-sdk-content
description: Describes the level of GPU-based validation to perform at runtime.
old-location: direct3d12\d3d12_gpu_based_validation_flags.htm
tech.root: direct3d12
ms.assetid: D9FA7F77-8DE8-4630-A9C7-E95B9E997E23
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D3D12_GPU_BASED_VALIDATION_FLAGS, D3D12_GPU_BASED_VALIDATION_FLAGS enumeration, D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING, D3D12_GPU_BASED_VALIDATION_FLAGS_NONE, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_FLAGS_NONE, direct3d12.d3d12_gpu_based_validation_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_GPU_BASED_VALIDATION_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_GPU_BASED_VALIDATION_FLAGS
req.redist: 
---

# D3D12_GPU_BASED_VALIDATION_FLAGS enumeration


## -description


Describes the level of GPU-based validation to perform at runtime.


## -enum-fields




### -field D3D12_GPU_BASED_VALIDATION_FLAGS_NONE

Default behavior; resource states, descriptors, and descriptor tables are all validated.


### -field D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING

When set, GPU-based validation does not perform resource state validation which greatly reduces the performance cost of GPU-based validtion. Descriptors and descriptor heaps are still validated.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/EA774CC4-7675-46AA-9CDF-56C8B9507702">ID3D12Debug2::SetGPUBasedValidationFlags</a> method to configure the amount of runtime validation that will occur.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

