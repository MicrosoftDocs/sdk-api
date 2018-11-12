---
UID: NS:d3d12.D3D12_RAYTRACING_GEOMETRY_DESC
title: D3D12_RAYTRACING_GEOMETRY_DESC
author: windows-sdk-content
description: Describes a set of geometry that is used in the D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS structure to provide input data to a raytracing acceleration structure build operation.
old-location: direct3d12\d3d12_raytracing_geometry_desc.htm
tech.root: direct3d12
ms.assetid: 41E6348C-F0D0-4BA3-B24C-3844AE2B7423
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_RAYTRACING_GEOMETRY_DESC, D3D12_RAYTRACING_GEOMETRY_DESC structure, PD3D12_RAYTRACING_GEOMETRY_DESC, PD3D12_RAYTRACING_GEOMETRY_DESC structure pointer, d3d12/D3D12_RAYTRACING_GEOMETRY_DESC, d3d12/PD3D12_RAYTRACING_GEOMETRY_DESC, direct3d12.d3d12_raytracing_geometry_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RAYTRACING_GEOMETRY_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_RAYTRACING_GEOMETRY_DESC
req.redist: 
---

# D3D12_RAYTRACING_GEOMETRY_DESC structure


## -description


Describes a set of geometry that is used in the <a href="http://docs.microsoft.com/windows/desktop/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS</a> structure to provide input data to a raytracing acceleration structure build operation.


## -struct-fields




### -field Type

The type of geometry.


### -field Flags

The geometry flags


### -field Triangles

A <a href="http://docs.microsoft.com/windows/desktop/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc">D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC</a> describing triangle geometry, if <i>Type</i> is  <a href="http://docs.microsoft.com/windows/desktop/d3d12/ne-d3d12-d3d12_raytracing_geometry_type">D3D12_RAYTRACING_GEOMETRY_TYPE_TRIANGLES</a>.  Otherwise this parameter is unused. 


### -field AABBs

A <a href="http://docs.microsoft.com/windows/desktop/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc">D3D12_RAYTRACING_GEOMETRY_AABBS_DESC</a> describing triangle geometry, if <i>Type</i> is  <a href="http://docs.microsoft.com/windows/desktop/d3d12/ne-d3d12-d3d12_raytracing_geometry_type">D3D12_RAYTRACING_GEOMETRY_TYPE_PROCEDURAL_PRIMITIVE_AABBS</a>.  Otherwise this parameter is unused.

