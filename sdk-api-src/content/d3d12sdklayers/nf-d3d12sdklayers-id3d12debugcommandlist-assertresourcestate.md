---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D12DebugCommandList::AssertResourceState


## -description



          Checks whether a resource, or subresource, is in a specified state, or not.


## -parameters




### -param pResource [in]

Type: <b>ID3D12Resource*</b>

Specifies the  <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> to check.


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




<a href="https://msdn.microsoft.com/EDE527F0-4091-4B03-9030-6F693FE901BE">ID3D12DebugCommandList</a>
 

 

