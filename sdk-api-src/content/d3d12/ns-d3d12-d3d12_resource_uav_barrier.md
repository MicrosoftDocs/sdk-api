---
UID: NS:d3d12.D3D12_RESOURCE_UAV_BARRIER
title: D3D12_RESOURCE_UAV_BARRIER (d3d12.h)
description: Represents a resource in which all UAV accesses must complete before any future UAV accesses can begin.
helpviewer_keywords: ["D3D12_RESOURCE_UAV_BARRIER","D3D12_RESOURCE_UAV_BARRIER structure","d3d12/D3D12_RESOURCE_UAV_BARRIER","direct3d12.d3d12_resource_uav_barrier"]
old-location: direct3d12\d3d12_resource_uav_barrier.htm
tech.root: direct3d12
ms.assetid: 683F645F-9A90-4648-99EF-2F7444254B41
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_UAV_BARRIER, D3D12_RESOURCE_UAV_BARRIER structure, d3d12/D3D12_RESOURCE_UAV_BARRIER, direct3d12.d3d12_resource_uav_barrier
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
req.typenames: D3D12_RESOURCE_UAV_BARRIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_UAV_BARRIER
 - d3d12/D3D12_RESOURCE_UAV_BARRIER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RESOURCE_UAV_BARRIER
---

# D3D12_RESOURCE_UAV_BARRIER structure


## -description

Represents a resource in which all UAV accesses must complete before any future UAV accesses can begin.

## -struct-fields

### -field pResource

The resource used in the transition, as a pointer to <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>.

## -remarks

This struct represents a resource in which all unordered access view (UAV) accesses (reads or writes) must complete before any future UAV accesses (read or write) can begin.
      

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier">D3D12_RESOURCE_BARRIER</a> structure.
      

You don't need to insert a UAV barrier between 2 draw or dispatch calls that only read a UAV.
        Additionally, you don't need to insert a UAV barrier between 2 draw or dispatch calls that write to the same UAV if you know that it's safe to execute the UAV accesses in any order.
        The resource can be <b>NULL</b>, which indicates that any UAV access could require the barrier.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>