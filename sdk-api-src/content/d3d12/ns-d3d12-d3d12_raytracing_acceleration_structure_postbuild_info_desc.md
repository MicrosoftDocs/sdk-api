---
UID: NS:d3d12.D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC
title: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC (d3d12.h)
description: Description of the post-build information to generate from an acceleration structure. Use this structure in calls to EmitRaytracingAccelerationStructurePostbuildInfo and BuildRaytracingAccelerationStructure.
helpviewer_keywords: ["D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC structure","PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC","PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC structure pointer","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC","d3d12/PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC","direct3d12.d3d12_raytracing_acceleration_structure_postbuild_info_desc"]
old-location: direct3d12\d3d12_raytracing_acceleration_structure_postbuild_info_desc.htm
tech.root: direct3d12
ms.assetid: 95CF4A85-8770-4044-B807-D97C21E80321
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC structure, PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC, PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC structure pointer, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC, d3d12/PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC, direct3d12.d3d12_raytracing_acceleration_structure_postbuild_info_desc
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
req.typenames: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC
 - d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC
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
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC
---

# D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC structure


## -description

Description of the post-build information to generate from an acceleration structure.  Use this structure in calls to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a> and  <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure">BuildRaytracingAccelerationStructure</a>.

## -struct-fields

### -field DestBuffer

Storage for the post-build info result.  Size required and the layout of the contents written by the system depend on the value of the <i>InfoType</i> field.

The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_UNORDERED_ACCESS</a>.  The memory must be aligned to the natural alignment for the members of the particular output structure being generated (e.g. 8 bytes for a struct with the largest members being UINT64).

### -field InfoType

A [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type) value specifying the type of post-build information to retrieve.
