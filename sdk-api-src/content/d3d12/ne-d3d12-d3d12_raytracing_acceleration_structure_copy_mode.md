---
UID: NE:d3d12.D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE
title: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE (d3d12.h)
description: Specifies the type of copy operation performed when calling CopyRaytracingAccelerationStructure.
helpviewer_keywords: ["D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE enumeration","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_CLONE","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_COMPACT","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_DESERIALIZE","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_SERIALIZE","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_VISUALIZATION_DECODE_FOR_TOOLS","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_CLONE","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_COMPACT","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_DESERIALIZE","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_SERIALIZE","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_VISUALIZATION_DECODE_FOR_TOOLS","direct3d12.d3d12_raytracing_acceleration_structure_copy_mode"]
old-location: direct3d12\d3d12_raytracing_acceleration_structure_copy_mode.htm
tech.root: direct3d12
ms.assetid: 93F2947F-3076-4109-AC6C-7BAA2D79B456
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE enumeration, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_CLONE, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_COMPACT, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_DESERIALIZE, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_SERIALIZE, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_VISUALIZATION_DECODE_FOR_TOOLS, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_CLONE, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_COMPACT, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_DESERIALIZE, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_SERIALIZE, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_VISUALIZATION_DECODE_FOR_TOOLS, direct3d12.d3d12_raytracing_acceleration_structure_copy_mode
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
req.typenames: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE
 - d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE
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
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE
---

# D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE enumeration


## -description

Specifies the type of copy operation performed when calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure">CopyRaytracingAccelerationStructure</a>.

## -enum-fields

### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_CLONE:0

Copy an acceleration structure while fixing any self-referential pointers that may be present so that the destination is a self-contained copy of the source.  Any external pointers to other acceleration structures remain unchanged from source to destination in the copy.  The size of the destination is identical to the size of the source.

> [!IMPORTANT]
> The source memory must be in state [**D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).
> The destination memory must be in state [**D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_COMPACT:0x1

Produces a functionally equivalent acceleration structure to source in the destination, similar to the clone mode, but also fits the destination into a potentially smaller, and certainly not larger, memory footprint.  The size required for the destination can be retrieved beforehand from <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a>.

This mode is only valid if the source acceleration structure was originally built with the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAG_ALLOW_COMPACTION</a>  flag, otherwise results are undefined.

Compacting geometry requires the entire acceleration structure to be constructed, which is why you must first build and then compact the structure.

> [!IMPORTANT]
> The source memory must be in state [**D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).
> The destination memory must be in state [**D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_VISUALIZATION_DECODE_FOR_TOOLS:0x2

The destination is takes  the layout described in <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_tools_visualization_header">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_TOOLS_VISUALIZATION_HEADER</a>.  The size required for the destination can be retrieved beforehand from <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a>.

This mode is only intended for tools such as PIX, though nothing stops any app from using it.  The output is essentially the inverse of an acceleration structure build.  This overall structure with is sufficient for tools/PIX to be able to give the application some visual sense of the acceleration structure the driver made out of the app’s input.  Visualization can help reveal driver bugs in acceleration structures if what is shown grossly mismatches the data the application used to create the acceleration structure, beyond allowed tolerances.

For top-level acceleration structures, the output includes a set of instance descriptions that are identical to the data used in the original build and in the same order.  For bottom-level acceleration structures, the output includes a set of geometry descriptions roughly matching the data used in the original build.  The output is only a rough match for the original in part because of the tolerances allowed in the specification for acceleration structures and in part due to the inherent complexity of reporting exactly the same structure as is conceptually encoded.  For example. axis-aligned bounding boxes (AABBs) returned for procedural primitives could be more conservative (larger) in volume and even different in number than what is actually in the acceleration structure representation.  Geometries, each with its own geometry description, appear in the same order as in the original acceleration, as shader table indexing calculations depend on this.


> [!IMPORTANT]
> The source memory must be in state [**D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).
> The destination memory must be in state [**D3D12_RESOURCE_STATE_UNORDERED_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

This mode is only permitted when developer mode is enabled in the OS.

### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_SERIALIZE:0x3

Destination takes the layout and size described in the documentation for <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC</a>, itself a structure generated with a call to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a>. 

This mode serializes an acceleration structure so that an app or tools can store it to a file for later reuse, typically on a different device instance, via deserialization.

When serializing a top-level acceleration structure, the bottom-level acceleration structures it refers to do not have to still be present or intact in memory.  Likewise, bottom-level acceleration structures can be serialized independent of whether any top-level acceleration structures are pointing to them.  In other words, the order of serialization of acceleration structures doesn’t matter.

> [!IMPORTANT]
> The source memory must be in state [**D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).
> The destination memory must be in state [**D3D12_RESOURCE_STATE_UNORDERED_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_DESERIALIZE:0x4

The source must be a serialized acceleration structure, with any pointers, directly after the header, fixed to point to their new locations. For more information, see  <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC</a>.

The destination gets an acceleration structure that is functionally equivalent to the acceleration structure that was originally serialized.  It does not matter what order top-level and bottom-level acceleration structures are deserialized, as long as by the time a top-level acceleration structure is used for raytracing or acceleration structure updates the bottom-level acceleration structures it references are present.

Deserialization can only be performed on the same device and driver version on which the data was serialized. Otherwise, the results are undefined.  

This mode is only intended for tools such as PIX, though nothing stops any app from using it, but this mode is only permitted when developer mode is enabled in the OS.   This copy operation is not intended to be used for caching acceleration structures, because running a full acceleration structure build is likely to be faster than loading one from disk.  


> [!IMPORTANT]
> The source memory must be in state [**D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).
> The destination memory must be in state [**D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).
