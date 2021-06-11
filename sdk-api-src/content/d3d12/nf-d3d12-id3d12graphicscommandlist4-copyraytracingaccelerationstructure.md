---
UID: NF:d3d12.ID3D12GraphicsCommandList4.CopyRaytracingAccelerationStructure
title: ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure (d3d12.h)
description: Copies a source acceleration structure to destination memory while applying the specified transformation.
helpviewer_keywords: ["CopyRaytracingAccelerationStructure","CopyRaytracingAccelerationStructure method","CopyRaytracingAccelerationStructure method","ID3D12GraphicsCommandList4 interface","ID3D12GraphicsCommandList4 interface","CopyRaytracingAccelerationStructure method","ID3D12GraphicsCommandList4.CopyRaytracingAccelerationStructure","ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure","d3d12/ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure","direct3d12.id3d12graphicscommandlist4_copyraytracingaccelerationstructure"]
old-location: direct3d12\id3d12graphicscommandlist4_copyraytracingaccelerationstructure.htm
tech.root: direct3d12
ms.assetid: 13E0E477-9CD5-484B-9532-AB6D415CF6CB
ms.date: 12/05/2018
ms.keywords: CopyRaytracingAccelerationStructure, CopyRaytracingAccelerationStructure method, CopyRaytracingAccelerationStructure method,ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,CopyRaytracingAccelerationStructure method, ID3D12GraphicsCommandList4.CopyRaytracingAccelerationStructure, ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure, d3d12/ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure, direct3d12.id3d12graphicscommandlist4_copyraytracingaccelerationstructure
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure
 - d3d12/ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12GraphicsCommandList4.CopyRaytracingAccelerationStructure
---

# ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure


## -description

Copies a source acceleration structure to destination memory while applying the specified transformation.

## -parameters

### -param DestAccelerationStructureData [in]

The destination memory. The required size can be discovered by calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a> beforehand, if necessary for the specified <i>Mode</i>.  

The destination start address must be aligned to 256 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BYTE_ALIGNMENT</a>, regardless of the specified <i>Mode</i>. 

The destination memory range cannot overlap source. Otherwise, results are undefined.  

The resource state that the memory pointed to must be in depends on the <i>Mode</i> parameter. For more information, see <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE</a>.

### -param SourceAccelerationStructureData [in]

The address of the acceleration structure or other type of data to copy/transform based on the specified <i>Mode</i>.  The data remains unchanged and usable.  The operation only copies the data  pointed to by <i>SourceAccelerationStructureData</i> and not any other data, such as acceleration structures, that the source data may point to.  For example, in the case of a top-level acceleration structure, any bottom-level acceleration structures that it points to are not copied in the operation.

The source memory must be aligned to 256 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BYTE_ALIGNMENT</a>, regardless of the specified <i>Mode</i>. 

The resource state that the memory pointed to must be in depends on the <i>Mode</i> parameter. For more information, see <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE</a>.

### -param Mode [in]

The type of copy operation to perform. For more information, see <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE</a>.

## -remarks

Since raytracing acceleration structures may contain internal pointers and have a device dependent opaque layout, copying them around or otherwise manipulating them requires a dedicated API so that drivers can handle the requested operation.

This method can be called from graphics or compute command lists but not from bundles.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12graphicscommandlist4.md">ID3D12GraphicsCommandList4</a>
