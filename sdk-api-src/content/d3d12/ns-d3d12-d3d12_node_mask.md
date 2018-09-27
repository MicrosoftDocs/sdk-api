---
UID: NS:d3d12.D3D12_NODE_MASK
title: D3D12_NODE_MASK
author: windows-sdk-content
description: A state subobject that identifies the GPU nodes to which the state object applies.
old-location: direct3d12\d3d12_node_mask.htm
tech.root: direct3d12
ms.assetid: DB1CF496-EB74-4898-8742-6D8374455C00
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D12_NODE_MASK, D3D12_NODE_MASK structure, PD3D12_NODE_MASK, PD3D12_NODE_MASK structure pointer, d3d12/D3D12_NODE_MASK, d3d12/PD3D12_NODE_MASK, direct3d12.d3d12_node_mask
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
 - D3D12_NODE_MASK
product: Windows
targetos: Windows
req.typenames: D3D12_NODE_MASK
req.redist: 
---

# D3D12_NODE_MASK structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

A state subobject that identifies the GPU nodes to which the state object applies.


## -struct-fields




### -field NodeMask

The node mask.


## -remarks



This subobject is optional. In its absence, the state object applies to all available nodes.  If a node mask subobject has been associated with any part of a state object, a node mask association must be made to all exports in a state object (including imported collections) and all node mask subobjects that are referenced must have matching content. 



