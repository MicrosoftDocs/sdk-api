---
UID: NE:d3d12.D3D12_CROSS_NODE_SHARING_TIER
title: D3D12_CROSS_NODE_SHARING_TIER (d3d12.h)
description: Specifies the level of sharing across nodes of an adapter, such as Tier 1 Emulated, Tier 1, or Tier 2.
helpviewer_keywords: ["D3D12_CROSS_NODE_SHARING_TIER","D3D12_CROSS_NODE_SHARING_TIER enumeration","D3D12_CROSS_NODE_SHARING_TIER_1","D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED","D3D12_CROSS_NODE_SHARING_TIER_2","D3D12_CROSS_NODE_SHARING_TIER_NOT_SUPPORTED","d3d12/D3D12_CROSS_NODE_SHARING_TIER","d3d12/D3D12_CROSS_NODE_SHARING_TIER_1","d3d12/D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED","d3d12/D3D12_CROSS_NODE_SHARING_TIER_2","d3d12/D3D12_CROSS_NODE_SHARING_TIER_NOT_SUPPORTED","direct3d12.d3d12_cross_node_sharing_tier"]
old-location: direct3d12\d3d12_cross_node_sharing_tier.htm
tech.root: direct3d12
ms.assetid: 49DAC69D-8134-4D1E-94B6-443978C24073
ms.date: 12/05/2018
ms.keywords: D3D12_CROSS_NODE_SHARING_TIER, D3D12_CROSS_NODE_SHARING_TIER enumeration, D3D12_CROSS_NODE_SHARING_TIER_1, D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED, D3D12_CROSS_NODE_SHARING_TIER_2, D3D12_CROSS_NODE_SHARING_TIER_NOT_SUPPORTED, d3d12/D3D12_CROSS_NODE_SHARING_TIER, d3d12/D3D12_CROSS_NODE_SHARING_TIER_1, d3d12/D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED, d3d12/D3D12_CROSS_NODE_SHARING_TIER_2, d3d12/D3D12_CROSS_NODE_SHARING_TIER_NOT_SUPPORTED, direct3d12.d3d12_cross_node_sharing_tier
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
req.typenames: D3D12_CROSS_NODE_SHARING_TIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_CROSS_NODE_SHARING_TIER
 - d3d12/D3D12_CROSS_NODE_SHARING_TIER
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
 - D3D12_CROSS_NODE_SHARING_TIER
---

## -description

Specifies the level of sharing across nodes of an adapter, such as Tier 1 Emulated, Tier 1, or Tier 2.

## -enum-fields

### -field D3D12_CROSS_NODE_SHARING_TIER_NOT_SUPPORTED:0

If an adapter has only 1 node, then cross-node sharing doesn't apply, so the <b>CrossNodeSharingTier</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure is set to D3D12_CROSS_NODE_SHARING_NOT_SUPPORTED.

### -field D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED:1

Tier 1 Emulated. Devices that set the <b>CrossNodeSharingTier</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure to D3D12_CROSS_NODE_SHARING_TIER_1_EMULATED have Tier 1 support.
However, drivers stage these copy operations through a driver-internal system memory allocation. This will cause these copy operations to consume time on the destination GPU as well as the source.

### -field D3D12_CROSS_NODE_SHARING_TIER_1:2

Tier 1. Devices that set the <b>CrossNodeSharingTier</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure to D3D12_CROSS_NODE_SHARING_TIER_1 only support the following cross-node copy operations:

<ul>
<li><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion">ID3D12CommandList::CopyBufferRegion</a></li>
<li><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">ID3D12CommandList::CopyTextureRegion</a></li>
<li><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource">ID3D12CommandList::CopyResource</a></li>
</ul>

Additionally, the cross-node resource must be the destination of the copy operation.

### -field D3D12_CROSS_NODE_SHARING_TIER_2:3

Tier 2. Devices that set the <b>CrossNodeSharingTier</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure to D3D12_CROSS_NODE_SHARING_TIER_2 support all operations across nodes, except for the following:

<ul>
<li>Render target views.</li>
<li>Depth stencil views.</li>
<li>UAV atomic operations. Similar to CPU/GPU interop, shaders may perform UAV atomic operations; however, no atomicity across adapters is guaranteed.</li>
</ul>
Applications can retrieve the node where a resource/heap exists from the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc">D3D12_HEAP_DESC</a> structure. These values are retrievable for opened resources. The runtime performs the appropriate re-mapping in case the 2 devices are using different UMD-specified node re-mappings.

### -field D3D12_CROSS_NODE_SHARING_TIER_3:4

Indicates support for [**D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS**](./ne-d3d12-d3d12_heap_flags.md) on heaps that are visible to multiple nodes.

## -remarks

This enum is used by the <b>CrossNodeSharingTier</b> member of the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
