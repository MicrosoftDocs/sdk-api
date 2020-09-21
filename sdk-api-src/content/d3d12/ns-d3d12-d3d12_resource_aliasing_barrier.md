---
UID: NS:d3d12.D3D12_RESOURCE_ALIASING_BARRIER
title: D3D12_RESOURCE_ALIASING_BARRIER (d3d12.h)
description: Describes the transition between usages of two different resources that have mappings into the same heap.
helpviewer_keywords: ["D3D12_RESOURCE_ALIASING_BARRIER","D3D12_RESOURCE_ALIASING_BARRIER structure","d3d12/D3D12_RESOURCE_ALIASING_BARRIER","direct3d12.d3d12_resource_aliasing_barrier"]
old-location: direct3d12\d3d12_resource_aliasing_barrier.htm
tech.root: direct3d12
ms.assetid: 9855D609-E863-4334-B6BA-B6777FDAB82B
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_ALIASING_BARRIER, D3D12_RESOURCE_ALIASING_BARRIER structure, d3d12/D3D12_RESOURCE_ALIASING_BARRIER, direct3d12.d3d12_resource_aliasing_barrier
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
req.typenames: D3D12_RESOURCE_ALIASING_BARRIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_ALIASING_BARRIER
 - d3d12/D3D12_RESOURCE_ALIASING_BARRIER
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
 - D3D12_RESOURCE_ALIASING_BARRIER
---

# D3D12_RESOURCE_ALIASING_BARRIER structure


## -description

Describes the transition between usages of two different resources that have mappings into the same heap.

## -struct-fields

### -field pResourceBefore

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> object that represents the before resource used in the transition.

### -field pResourceAfter

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> object that represents the after resource used in the transition.

## -remarks

This structure is a member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier">D3D12_RESOURCE_BARRIER</a> structure.
      

Both the before and the after resources can be specified or one or both resources can be <b>NULL</b>, which indicates that any placed or reserved resource could cause aliasing.
      

Refer to the usage models described in <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12">Using Resource Barriers to Synchronize Resource States in Direct3D 12</a>