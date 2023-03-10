---
UID: NS:d3d12.D3D12_RESOURCE_BARRIER
title: D3D12_RESOURCE_BARRIER (d3d12.h)
description: Describes a resource barrier (transition in resource use).
helpviewer_keywords: ["D3D12_RESOURCE_BARRIER","D3D12_RESOURCE_BARRIER structure","d3d12/D3D12_RESOURCE_BARRIER","direct3d12.d3d12_resource_barrier"]
old-location: direct3d12\d3d12_resource_barrier.htm
tech.root: direct3d12
ms.assetid: 49F02D65-767E-4BA4-A90D-68AA2D709E09
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_BARRIER, D3D12_RESOURCE_BARRIER structure, d3d12/D3D12_RESOURCE_BARRIER, direct3d12.d3d12_resource_barrier
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
req.typenames: D3D12_RESOURCE_BARRIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_BARRIER
 - d3d12/D3D12_RESOURCE_BARRIER
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
 - D3D12_RESOURCE_BARRIER
---

# D3D12_RESOURCE_BARRIER structure


## -description

Describes a resource barrier (transition in resource use).

## -struct-fields

### -field Type

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_type">D3D12_RESOURCE_BARRIER_TYPE</a>-typed value that specifies the type of resource barrier. 
            This member determines which type to use in the union below.

### -field Flags

Specifies a <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags">D3D12_RESOURCE_BARRIER_FLAGS</a> enumeration constant such as for "begin only" or "end only".

### -field Transition

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier">D3D12_RESOURCE_TRANSITION_BARRIER</a> structure that describes the transition of subresources between different usages.  
              Members specify the before and after usages of the subresources.

### -field Aliasing

A 
              <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier">D3D12_RESOURCE_ALIASING_BARRIER</a> structure that describes the transition between usages of two different resources that have mappings into the same heap.

### -field UAV

A 
              <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier">D3D12_RESOURCE_UAV_BARRIER</a> structure that describes a resource in which all UAV accesses (reads or writes) must complete before any future UAV accesses (read or write) can begin.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier">ID3D12GraphicsCommandList::ResourceBarrier</a> method.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>