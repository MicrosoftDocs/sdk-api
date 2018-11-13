---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList1.AssertResourceState
title: ID3D12DebugCommandList1::AssertResourceState
author: windows-sdk-content
description: Validates that the given state matches the state of the subresource, assuming the state of the given subresource is known during recording of a command list (e.g.
old-location: direct3d12\id3d12debugcommandlist1_assertresourcestate.htm
tech.root: direct3d12
ms.assetid: DB036A55-D677-4288-B165-5441BA457492
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AssertResourceState, AssertResourceState method, AssertResourceState method,ID3D12DebugCommandList1 interface, ID3D12DebugCommandList1 interface,AssertResourceState method, ID3D12DebugCommandList1.AssertResourceState, ID3D12DebugCommandList1::AssertResourceState, d3d12sdklayers/ID3D12DebugCommandList1::AssertResourceState, direct3d12.id3d12debugcommandlist1_assertresourcestate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugCommandList1.AssertResourceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugCommandList1::AssertResourceState


## -description


Validates that the given state matches the state of the subresource, assuming the state of the given subresource is known during recording of a command list (e.g. the resource was transitioned earlier in the same command list recording).  If the state is not yet known this method sets the known state for further validation later in the same command list recording.


## -parameters




### -param pResource [in]

Type: <b>ID3D12Resource*</b>

Specifies the <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> to check.


### -param Subresource

Type: <b>UINT</b>

The index of the subresource to check. This can be set to an index, or D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES.


### -param State

Type: <b>UINT</b>

Specifies the state to check for. This can be one or more <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATES</a> flags Or'ed together.


## -returns



Type: <b>BOOL</b>

This method returns <b>true</b> if the tracked state of the resource or subresource matches the specified state, <b>false</b> otherwise.




## -remarks



Since execution of command lists occurs sometime after recording, the state of a resource often cannot be known during command list recording.  <b>AssertResourceState</b> gives an application developer the ability to impose an assumed state on a resource or subresource at a fixed recording point in a command list.

Often the state of a resource or subresource can either be known due to a previous barrier or inferred-by-use (for example, was used in an earlier call to <a href="https://msdn.microsoft.com/46F89B85-EDAA-4095-B6C6-4CC47F972F09">CopyBufferRegion</a>) during command list recording.  In such cases <b>AssertResourceState</b> can produce a debug message if the given state does not match the known or assumed state.

This API is for debug validation only and does not affect the actual runtime or GPU state of the resource.




## -see-also




<a href="https://msdn.microsoft.com/2DF22383-768C-4D23-9ED8-F0CFD6BA6EE7">ID3D12DebugCommandList1</a>
 

 

