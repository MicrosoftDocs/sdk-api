---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList1.AssertResourceState
title: ID3D12DebugCommandList1::AssertResourceState (d3d12sdklayers.h)
description: Validates that the given state matches the state of the subresource, assuming the state of the given subresource is known during recording of a command list (e.g.
helpviewer_keywords: ["AssertResourceState","AssertResourceState method","AssertResourceState method","ID3D12DebugCommandList1 interface","ID3D12DebugCommandList1 interface","AssertResourceState method","ID3D12DebugCommandList1.AssertResourceState","ID3D12DebugCommandList1::AssertResourceState","d3d12sdklayers/ID3D12DebugCommandList1::AssertResourceState","direct3d12.id3d12debugcommandlist1_assertresourcestate"]
old-location: direct3d12\id3d12debugcommandlist1_assertresourcestate.htm
tech.root: direct3d12
ms.assetid: DB036A55-D677-4288-B165-5441BA457492
ms.date: 12/05/2018
ms.keywords: AssertResourceState, AssertResourceState method, AssertResourceState method,ID3D12DebugCommandList1 interface, ID3D12DebugCommandList1 interface,AssertResourceState method, ID3D12DebugCommandList1.AssertResourceState, ID3D12DebugCommandList1::AssertResourceState, d3d12sdklayers/ID3D12DebugCommandList1::AssertResourceState, direct3d12.id3d12debugcommandlist1_assertresourcestate
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
 - ID3D12DebugCommandList1::AssertResourceState
 - d3d12sdklayers/ID3D12DebugCommandList1::AssertResourceState
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
 - ID3D12DebugCommandList1.AssertResourceState
---

# ID3D12DebugCommandList1::AssertResourceState


## -description

Validates that the given state matches the state of the subresource, assuming the state of the given subresource is known during recording of a command list (e.g. the resource was transitioned earlier in the same command list recording).  If the state is not yet known this method sets the known state for further validation later in the same command list recording.

## -parameters

### -param pResource [in]

Type: <b>ID3D12Resource*</b>

Specifies the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> to check.

### -param Subresource

Type: <b>UINT</b>

The index of the subresource to check. This can be set to an index, or D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES.

### -param State

Type: <b>UINT</b>

Specifies the state to check for. This can be one or more <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a> flags Or'ed together.

## -returns

Type: <b>BOOL</b>

This method returns <b>true</b> if the tracked state of the resource or subresource matches the specified state, <b>false</b> otherwise.

## -remarks

Since execution of command lists occurs sometime after recording, the state of a resource often cannot be known during command list recording.  <b>AssertResourceState</b> gives an application developer the ability to impose an assumed state on a resource or subresource at a fixed recording point in a command list.

Often the state of a resource or subresource can either be known due to a previous barrier or inferred-by-use (for example, was used in an earlier call to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion">CopyBufferRegion</a>) during command list recording.  In such cases <b>AssertResourceState</b> can produce a debug message if the given state does not match the known or assumed state.

This API is for debug validation only and does not affect the actual runtime or GPU state of the resource.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1">ID3D12DebugCommandList1</a>