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

# ID3D12DebugCommandQueue::AssertResourceState


## -description



          Checks whether a resource, or subresource, is in a specified state, or not.


## -parameters




### -param pResource [in]

Type: <b>ID3D12Resource*</b>


            Specifies the  <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a> to check.


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



This method is very similar to <a href="https://msdn.microsoft.com/9190760D-B624-4E3E-8C33-B5D888895499">ID3D12DebugCommandList::AssertResourceState</a>, however there are methods on the command queue that work directly with resources that might need to be monitored (for example <a href="https://msdn.microsoft.com/FAFA4B5C-EA3C-4209-AB8E-75F3B90F3745">ID3D13CommandQueue::CopyTileMappings</a>).




## -see-also




<a href="https://msdn.microsoft.com/383F3B25-10C6-464C-AB79-D35F6FD3E879">ID3D12DebugCommandQueue</a>
 

 

