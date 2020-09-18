---
UID: NS:d3d12.D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS
title: D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS (d3d12.h)
description: Defines the inputs for a raytracing acceleration structure build operation. This structure is used by ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure and ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo.
helpviewer_keywords: ["D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS","D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS structure","PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS","PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS structure pointer","d3d12/D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS","d3d12/PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS","direct3d12.d3d12_build_raytracing_acceleration_structure_inputs"]
old-location: direct3d12\d3d12_build_raytracing_acceleration_structure_inputs.htm
tech.root: direct3d12
ms.assetid: C6781F5B-A3B6-4630-A94F-C438AEA62EB7
ms.date: 12/05/2018
ms.keywords: D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS, D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS structure, PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS, PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS structure pointer, d3d12/D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS, d3d12/PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS, direct3d12.d3d12_build_raytracing_acceleration_structure_inputs
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
req.typenames: D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS
 - d3d12/D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS
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
 - D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS
---

# D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS structure


## -description

Defines the inputs for a raytracing acceleration structure build operation. This structure is used by <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure">ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure</a> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo">ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo</a>.

## -struct-fields

### -field Type

The type of acceleration structure to build.

### -field Flags

The build flags.

### -field NumDescs

If <i>Type</i> is <b>D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TOP_LEVEL</b>, this value is the number of instances, laid out based on <i>DescsLayout</i>.

If <i>Type</i> is <b>D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BOTTOM_LEVEL</b>, this value is the number of elements referred to by <i>pGeometryDescs</i> or <i>ppGeometryDescs</i>. Which of these fields  is used depends on <i>DescsLayout</i>.

### -field DescsLayout

How geometry descriptions are specified; either an array of descriptions or an array of pointers to descriptions.

### -field InstanceDescs

If <i>Type</i> is <b>D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TOP_LEVEL</b>, this refers to <i>NumDescs</i><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc">D3D12_RAYTRACING_INSTANCE_DESC</a> structures in GPU memory describing instances.  Each instance must be aligned to 16 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_INSTANCE_DESC_BYTE_ALIGNMENT</a>.

If <i>Type</i> is not <b>D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TOP_LEVEL</b>, this parameter is unused.

If <i>DescLayout</i> is <b>D3D12_ELEMENTS_LAYOUT_ARRAY</b>, <i>InstanceDescs</i> points to an array of instance descriptions in GPU memory. 

If <i>DescLayout</i> is <b>D3D12_ELEMENTS_LAYOUT_ARRAY_OF_POINTERS</b>, <i>InstanceDescs</i> points to an array in GPU memory of <a href="/windows/desktop/direct3d12/d3d12_gpu_virtual_address">D3D12_GPU_VIRTUAL_ADDRESS</a> pointers to instance descriptions. 

The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</a>.

### -field pGeometryDescs

If <i>Type</i> is <b>D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BOTTOM_LEVEL</b>, and <i>DescsLayout</i> is <b>D3D12_ELEMENTS_LAYOUT_ARRAY</b>, this field is used and points to <i>NumDescs</i> contiguous <b>D3D12_RAYTRACING_GEOMETRY_DESC</b> structures on the CPU, describing individual geometries.   

If <i>Type</i> is not <b>D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BOTTOM_LEVEL</b> or <i>DescsLayout</i> is not <b>D3D12_ELEMENTS_LAYOUT_ARRAY</b>, this parameter is unused.

### -field ppGeometryDescs

If <i>Type</i> is <b>D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BOTTOM_LEVEL</b>, and <i>DescsLayout</i> is <b>D3D12_ELEMENTS_LAYOUT_ARRAY_OF_POINTERS</b>, this field is used and points to an array of <i>NumDescs</i> pointers to <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc">D3D12_RAYTRACING_GEOMETRY_DESC</a> structures on the CPU, describing individual geometries.

## -remarks

When used with  <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo">GetRaytracingAccelerationStructurePrebuildInfo</a>, which actually perform a build, any parameter that is referenced via <a href="/windows/desktop/direct3d12/d3d12_gpu_virtual_address">D3D12_GPU_VIRTUAL_ADDRESS</a> (an address in GPU memory), like <i>InstanceDescs</i>, will not be accessed by the operation.  So this memory does not need to be initialized yet or be in a particular resource state.  Whether GPU addresses are null or not can be inspected by the operation, even though the pointers are not dereferenced.