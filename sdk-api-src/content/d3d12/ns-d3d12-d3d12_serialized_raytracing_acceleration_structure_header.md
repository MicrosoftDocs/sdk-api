---
UID: NS:d3d12.D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER
title: D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER (d3d12.h)
description: Defines the header for a serialized raytracing acceleration structure.
helpviewer_keywords: ["D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER","D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER structure","PD3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER","PD3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER structure pointer","d3d12/D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER","d3d12/PD3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER","direct3d12.d3d12_serialized_raytracing_acceleration_structure_header"]
old-location: direct3d12\d3d12_serialized_raytracing_acceleration_structure_header.htm
tech.root: direct3d12
ms.assetid: 229AF9C0-DB24-4C11-A87D-15746B1544E7
ms.date: 12/05/2018
ms.keywords: D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER, D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER structure, PD3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER, PD3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER structure pointer, d3d12/D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER, d3d12/PD3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER, direct3d12.d3d12_serialized_raytracing_acceleration_structure_header
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
req.typenames: D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER
 - d3d12/D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER
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
 - D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER
---

# D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER structure


## -description

Defines the header for a serialized raytracing acceleration structure.

## -struct-fields

### -field DriverMatchingIdentifier

The driver-matching identifier.

### -field SerializedSizeInBytesIncludingHeader

The size of serialized data.

### -field DeserializedSizeInBytes

Size of the memory that will be consumed when the acceleration structure is deserialized.  This value is less than or equal to the size of the original acceleration structure before it was serialized.

### -field NumBottomLevelAccelerationStructurePointersAfterHeader

Size of the array of <a href="/windows/desktop/direct3d12/d3d12_gpu_virtual_address">D3D12_GPU_VIRTUAL_ADDRESS</a> values that follow the header.  For more information, see <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC</a>.