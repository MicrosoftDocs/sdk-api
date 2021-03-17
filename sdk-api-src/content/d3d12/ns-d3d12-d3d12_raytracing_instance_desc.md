---
UID: NS:d3d12.D3D12_RAYTRACING_INSTANCE_DESC
title: D3D12_RAYTRACING_INSTANCE_DESC (d3d12.h)
description: Describes an instance of a raytracing acceleration structure used in GPU memory during the acceleration structure build process.
helpviewer_keywords: ["D3D12_RAYTRACING_INSTANCE_DESC","D3D12_RAYTRACING_INSTANCE_DESC structure","PD3D12_RAYTRACING_INSTANCE_DESC","PD3D12_RAYTRACING_INSTANCE_DESC structure pointer","d3d12/D3D12_RAYTRACING_INSTANCE_DESC","d3d12/PD3D12_RAYTRACING_INSTANCE_DESC","direct3d12.d3d12_raytracing_instance_desc"]
old-location: direct3d12\d3d12_raytracing_instance_desc.htm
tech.root: direct3d12
ms.assetid: 816B0281-EC69-4EA1-AE32-6B3E178117DE
ms.date: 08/26/2019
ms.keywords: D3D12_RAYTRACING_INSTANCE_DESC, D3D12_RAYTRACING_INSTANCE_DESC structure, PD3D12_RAYTRACING_INSTANCE_DESC, PD3D12_RAYTRACING_INSTANCE_DESC structure pointer, d3d12/D3D12_RAYTRACING_INSTANCE_DESC, d3d12/PD3D12_RAYTRACING_INSTANCE_DESC, direct3d12.d3d12_raytracing_instance_desc
req.header: d3d12.h
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
req.typenames: D3D12_RAYTRACING_INSTANCE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_INSTANCE_DESC
 - d3d12/D3D12_RAYTRACING_INSTANCE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RAYTRACING_INSTANCE_DESC
---

# D3D12_RAYTRACING_INSTANCE_DESC structure


## -description

Describes an instance of a raytracing acceleration structure used in GPU memory during the acceleration structure build process.

## -struct-fields

### -field Transform

Type: **[FLOAT](/windows/win32/winprog/windows-data-types) \[3\]\[4\]**

A 3x4 transform matrix in row-major layout representing the instance-to-world transformation. Implementations transform rays, as opposed to transforming all of the geometry or AABBs.

> [!NOTE]
> The layout of `Transform` is a transpose of how affine matrices are typically stored in memory. Instead of four 3-vectors, `Transform` is laid out as three 4-vectors.

### -field InstanceID

Type: **[UINT](/windows/win32/winprog/windows-data-types) : 24**

An arbitrary 24-bit value that can be accessed using the `InstanceID` intrinsic function in supported shader types.

### -field InstanceMask

Type: **[UINT](/windows/win32/winprog/windows-data-types) : 8**

An 8-bit mask assigned to the instance, which can be used to include/reject groups of instances on a per-ray basis. If the value is zero, then the instance will never be included, so typically this should be set to some non-zero value. For more information see, the `InstanceInclusionMask` parameter to the [TraceRay](/windows/win32/direct3d12/traceray-function) function.

### -field InstanceContributionToHitGroupIndex

Type: **[UINT](/windows/win32/winprog/windows-data-types) : 24**

An arbitrary 24-bit value representing per-instance contribution to add into shader table indexing to select the hit group to use.

### -field Flags

Type: **[UINT](/windows/win32/winprog/windows-data-types) : 8**

An 8-bit mask representing flags from [D3D12_RAYTRACING_INSTANCE_FLAGS](./ne-d3d12-d3d12_raytracing_instance_flags.md) to apply to the instance.

### -field AccelerationStructure

Type: **[D3D12_GPU_VIRTUAL_ADDRESS](/windows/win32/direct3d12/d3d12_gpu_virtual_address)**

Address of the bottom-level acceleration structure that is being instanced. The address must be aligned to 256 bytes, defined as [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BYTE_ALIGNMENT](/windows/win32/direct3d12/constants). Any existing acceleration structure passed in here would already have been required to be placed with such alignment.

The memory pointed to must be in state [D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE](./ne-d3d12-d3d12_resource_states.md).

## -remarks

This C++ struct definition is useful if you're generating instance data on the CPU first, then uploading to the GPU. But your application is also free to generate instance descriptions directly into GPU memory (from compute shaders, for instance) following the same layout.