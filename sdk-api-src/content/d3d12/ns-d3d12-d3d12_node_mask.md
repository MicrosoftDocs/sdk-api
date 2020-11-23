---
UID: NS:d3d12.D3D12_NODE_MASK
title: D3D12_NODE_MASK (d3d12.h)
description: A state subobject that identifies the GPU nodes to which the state object applies.
helpviewer_keywords: ["D3D12_NODE_MASK","D3D12_NODE_MASK structure","PD3D12_NODE_MASK","PD3D12_NODE_MASK structure pointer","d3d12/D3D12_NODE_MASK","d3d12/PD3D12_NODE_MASK","direct3d12.d3d12_node_mask"]
old-location: direct3d12\d3d12_node_mask.htm
tech.root: direct3d12
ms.assetid: DB1CF496-EB74-4898-8742-6D8374455C00
ms.date: 12/05/2018
ms.keywords: D3D12_NODE_MASK, D3D12_NODE_MASK structure, PD3D12_NODE_MASK, PD3D12_NODE_MASK structure pointer, d3d12/D3D12_NODE_MASK, d3d12/PD3D12_NODE_MASK, direct3d12.d3d12_node_mask
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
req.typenames: D3D12_NODE_MASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_NODE_MASK
 - d3d12/D3D12_NODE_MASK
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
 - D3D12_NODE_MASK
---

# D3D12_NODE_MASK structure


## -description

A state subobject that identifies the GPU nodes to which the state object applies.

## -struct-fields

### -field NodeMask

The node mask.

## -remarks

This subobject is optional. In its absence, the state object applies to all available nodes.  If a node mask subobject has been associated with any part of a state object, a node mask association must be made to all exports in a state object (including imported collections) and all node mask subobjects that are referenced must have matching content.

> [!IMPORTANT]
> On some versions of the DirectX Runtime, specifying a node via **D3D12_NODE_MASK** in a [**D3D12_STATE_SUBOBJECT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) with type [**D3D12_STATE_SUBOBJECT_TYPE_NODE_MASK**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type), the runtime will incorrectly handle a node mask value of `0`, which should use node #1, which will lead to errors when attempting to use the state object later. Specify an explicit node value of 1, or omit the **D3D12_NODE_MASK** subobject to avoid this issue.
