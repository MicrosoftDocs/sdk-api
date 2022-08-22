---
UID: NF:d3d12sdklayers.ID3D12DebugCommandQueue.AssertResourceState
title: ID3D12DebugCommandQueue::AssertResourceState (d3d12sdklayers.h)
description: Checks whether a resource, or subresource, is in a specified state, or not. (ID3D12DebugCommandQueue.AssertResourceState)
helpviewer_keywords: ["AssertResourceState","AssertResourceState method","AssertResourceState method","ID3D12DebugCommandQueue interface","ID3D12DebugCommandQueue interface","AssertResourceState method","ID3D12DebugCommandQueue.AssertResourceState","ID3D12DebugCommandQueue::AssertResourceState","d3d12sdklayers/ID3D12DebugCommandQueue::AssertResourceState","direct3d12.id3d12debugcommandqueue_assertresourcestate"]
old-location: direct3d12\id3d12debugcommandqueue_assertresourcestate.htm
tech.root: direct3d12
ms.assetid: D96DE885-D3B3-4EE5-A119-54F4261D7056
ms.date: 12/05/2018
ms.keywords: AssertResourceState, AssertResourceState method, AssertResourceState method,ID3D12DebugCommandQueue interface, ID3D12DebugCommandQueue interface,AssertResourceState method, ID3D12DebugCommandQueue.AssertResourceState, ID3D12DebugCommandQueue::AssertResourceState, d3d12sdklayers/ID3D12DebugCommandQueue::AssertResourceState, direct3d12.id3d12debugcommandqueue_assertresourcestate
req.header: d3d12sdklayers.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12DebugCommandQueue::AssertResourceState
 - d3d12sdklayers/ID3D12DebugCommandQueue::AssertResourceState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugCommandQueue.AssertResourceState
---

# ID3D12DebugCommandQueue::AssertResourceState


## -description

Checks whether a resource, or subresource, is in a specified state, or not.

## -parameters

### -param pResource [in]

Type: <b>ID3D12Resource*</b>

Specifies the  <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> to check.

### -param Subresource

Type: <b>UINT</b>

The index of the subresource to check.
          This can be set to an index, or D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES.

### -param State

Type: <b>UINT</b>

Specifies the state to check for. This can be one or more D3D12_RESOURCE_STATES flags Or'ed together.

## -returns

Type: <b>BOOL</b>

This method returns true if the resource or subresource is in the specified state, false otherwise.

## -remarks

This method is very similar to <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist-assertresourcestate">ID3D12DebugCommandList::AssertResourceState</a>, however there are methods on the command queue that work directly with resources that might need to be monitored (for example <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">ID3D12CommandQueue::CopyTileMappings</a>).

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue">ID3D12DebugCommandQueue</a>
