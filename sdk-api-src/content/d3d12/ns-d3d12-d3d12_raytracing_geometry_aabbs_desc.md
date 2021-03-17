---
UID: NS:d3d12.D3D12_RAYTRACING_GEOMETRY_AABBS_DESC
title: D3D12_RAYTRACING_GEOMETRY_AABBS_DESC (d3d12.h)
description: Describes a set of Axis-aligned bounding boxes that are used in the D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS structure to provide input data to a raytracing acceleration structure build operation.
helpviewer_keywords: ["D3D12_RAYTRACING_GEOMETRY_AABBS_DESC","D3D12_RAYTRACING_GEOMETRY_AABBS_DESC structure","PD3D12_RAYTRACING_GEOMETRY_AABBS_DESC","PD3D12_RAYTRACING_GEOMETRY_AABBS_DESC structure pointer","d3d12/D3D12_RAYTRACING_GEOMETRY_AABBS_DESC","d3d12/PD3D12_RAYTRACING_GEOMETRY_AABBS_DESC","direct3d12.d3d12_raytracing_geometry_aabbs_desc"]
old-location: direct3d12\d3d12_raytracing_geometry_aabbs_desc.htm
tech.root: direct3d12
ms.assetid: A9FA270E-2B97-4DAC-891F-0DF83F8F9522
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_GEOMETRY_AABBS_DESC, D3D12_RAYTRACING_GEOMETRY_AABBS_DESC structure, PD3D12_RAYTRACING_GEOMETRY_AABBS_DESC, PD3D12_RAYTRACING_GEOMETRY_AABBS_DESC structure pointer, d3d12/D3D12_RAYTRACING_GEOMETRY_AABBS_DESC, d3d12/PD3D12_RAYTRACING_GEOMETRY_AABBS_DESC, direct3d12.d3d12_raytracing_geometry_aabbs_desc
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
req.typenames: D3D12_RAYTRACING_GEOMETRY_AABBS_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_GEOMETRY_AABBS_DESC
 - d3d12/D3D12_RAYTRACING_GEOMETRY_AABBS_DESC
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
 - D3D12_RAYTRACING_GEOMETRY_AABBS_DESC
---

# D3D12_RAYTRACING_GEOMETRY_AABBS_DESC structure


## -description

Describes a set of Axis-aligned bounding boxes that are used in the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS</a> structure to provide input data to a raytracing acceleration structure build operation.

## -struct-fields

### -field AABBCount

The number of AABBs pointed to in the contiguous array at <i>AABBs</i>.

### -field AABBs

the GPU memory location where an array of AABB descriptions is to be found, including the data stride between AABBs.  The address and stride must each be aligned to 8 bytes, defined as The address must be aligned to 16 bytes, defined as <a href="/windows/desktop/direct3d12/constants"> D3D12_RAYTRACING_AABB_BYTE_ALIGNMENT</a>.  The stride can be 0.