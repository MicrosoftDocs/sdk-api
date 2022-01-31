---
UID: NE:d3d12.D3D12_RESOURCE_HEAP_TIER
title: D3D12_RESOURCE_HEAP_TIER (d3d12.h)
description: Specifies which resource heap tier the hardware and driver support.
helpviewer_keywords: ["D3D12_RESOURCE_HEAP_TIER","D3D12_RESOURCE_HEAP_TIER enumeration","D3D12_RESOURCE_HEAP_TIER_1","D3D12_RESOURCE_HEAP_TIER_2","d3d12/D3D12_RESOURCE_HEAP_TIER","d3d12/D3D12_RESOURCE_HEAP_TIER_1","d3d12/D3D12_RESOURCE_HEAP_TIER_2","direct3d12.d3d12_resource_heap_tier"]
old-location: direct3d12\d3d12_resource_heap_tier.htm
tech.root: direct3d12
ms.assetid: 47C5B30C-BFFE-437A-878B-FE49F8EFFD02
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_HEAP_TIER, D3D12_RESOURCE_HEAP_TIER enumeration, D3D12_RESOURCE_HEAP_TIER_1, D3D12_RESOURCE_HEAP_TIER_2, d3d12/D3D12_RESOURCE_HEAP_TIER, d3d12/D3D12_RESOURCE_HEAP_TIER_1, d3d12/D3D12_RESOURCE_HEAP_TIER_2, direct3d12.d3d12_resource_heap_tier
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
req.typenames: D3D12_RESOURCE_HEAP_TIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_HEAP_TIER
 - d3d12/D3D12_RESOURCE_HEAP_TIER
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
 - D3D12_RESOURCE_HEAP_TIER
---

# D3D12_RESOURCE_HEAP_TIER enumeration


## -description

Specifies which resource heap tier the hardware and driver support.

## -enum-fields

### -field D3D12_RESOURCE_HEAP_TIER_1:1

Indicates that heaps can only support resources from a single resource category.
            For the list of resource categories, see Remarks.
            In tier 1, these resource categories are mutually exclusive and cannot be used with the same heap.
            The resource category must be declared when creating a heap, using the correct <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a> enumeration constant.
            Applications cannot create heaps with flags that allow all three categories.

### -field D3D12_RESOURCE_HEAP_TIER_2:2

Indicates that heaps can support resources from all three categories.
            For the list of resource categories, see Remarks.
            In tier 2, these resource categories can be mixed within the same heap.
            Applications may create heaps with flags that allow all three categories; but are not required to do so.
            Applications may be written to support tier 1 and seamlessly run on tier 2.

## -remarks

This enum is used by the <b>ResourceHeapTier</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
        

This enum specifies which resource heap tier the hardware and driver support.
          Lower tiers require more heap attribution than greater tiers.
        

Resources can be categorized into the following types:
        

<ul>
<li>Buffers</li>
<li>Non-render target &amp; non-depth stencil textures</li>
<li>Render target or depth stencil textures</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
