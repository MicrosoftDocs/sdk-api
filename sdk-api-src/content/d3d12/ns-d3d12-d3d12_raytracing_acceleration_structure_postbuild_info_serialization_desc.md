---
UID: NS:d3d12.D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC
title: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC (d3d12.h)
description: Describes the size and layout of the serialized acceleration structure and header.
helpviewer_keywords: ["D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC structure","PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC","PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC structure pointer","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC","d3d12/PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC","direct3d12.d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc"]
old-location: direct3d12\d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc.htm
tech.root: direct3d12
ms.assetid: F956D936-9946-4FEC-B0D1-ED522440B9E2
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC structure, PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC, PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC structure pointer, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC, d3d12/PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC, direct3d12.d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc
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
req.typenames: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC
 - d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC
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
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC
---

# D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC structure


## -description

Describes the size and layout of the serialized acceleration structure and header

## -struct-fields

### -field SerializedSizeInBytes

The size of the serialized acceleration structure, including a header.  The header is <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_serialized_raytracing_acceleration_structure_header">D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER</a> followed by followed by a list of pointers to bottom-level acceleration structures.

### -field NumBottomLevelAccelerationStructurePointers

The number of  64-bit GPU  virtual addresses that will be at the start of the serialized acceleration structure, after the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_serialized_raytracing_acceleration_structure_header">D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER</a>.  For a bottom-level acceleration structure this will be 0.  For a top-level acceleration structure, the pointers indicate the acceleration structures being referred to.  

When deserialization occurs, these pointers to bottom-level pointers must be initialized by the app in the serialized data (just after the header) to the new locations where the bottom level acceleration structures will reside.  It is not required that these new locations to have already been populated with bottom-level acceleration structures at deserialization time, as long as they are initialized with the expected deserialized data structures before being used in raytracing.  During deserialization, the driver reads the new pointers, using them to produce an equivalent top-level acceleration structure to the original.