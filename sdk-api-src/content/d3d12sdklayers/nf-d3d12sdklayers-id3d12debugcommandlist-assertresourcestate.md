---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList.AssertResourceState
title: ID3D12DebugCommandList::AssertResourceState
author: windows-sdk-content
description: Checks whether a resource, or subresource, is in a specified state, or not.
old-location: direct3d12\id3d12debugcommandlist_assertresourcestate.htm
tech.root: direct3d12
ms.assetid: 9190760D-B624-4E3E-8C33-B5D888895499
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AssertResourceState, AssertResourceState method, AssertResourceState method,ID3D12DebugCommandList interface, ID3D12DebugCommandList interface,AssertResourceState method, ID3D12DebugCommandList.AssertResourceState, ID3D12DebugCommandList::AssertResourceState, d3d12sdklayers/ID3D12DebugCommandList::AssertResourceState, direct3d12.id3d12debugcommandlist_assertresourcestate
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
 - ID3D12DebugCommandList.AssertResourceState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugCommandList::AssertResourceState


## -description


Checks whether a resource, or subresource, is in a specified state, or not.


## -parameters




### -param pResource [in]

Type: <b>ID3D12Resource*</b>

Specifies the  <a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a> to check.


### -param Subresource

Type: <b>UINT</b>

The index of the subresource to check. This can be set to an index, or D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES.


### -param State

Type: <b>UINT</b>

Specifies the state to check for. This can be one or more D3D12_RESOURCE_STATES flags Or'ed together.


## -returns



Type: <b>BOOL</b>

This method returns true if the resource or subresource is in the specified state, false otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950154(v=VS.85).aspx">ID3D12DebugCommandList</a>
 

 

