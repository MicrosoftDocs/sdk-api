---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.SetBreakOnID
title: ID3D12InfoQueue::SetBreakOnID
author: windows-sdk-content
description: Set a message identifier to break on when a message with that identifier passes through the storage filter.
old-location: direct3d12\id3d12infoqueue_setbreakonid.htm
old-project: direct3d12
ms.assetid: 227ECD21-AE8F-41D1-BF56-A516F14BFCD0
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12InfoQueue interface,SetBreakOnID method, ID3D12InfoQueue.SetBreakOnID, ID3D12InfoQueue::SetBreakOnID, SetBreakOnID, SetBreakOnID method, SetBreakOnID method,ID3D12InfoQueue interface, d3d12sdklayers/ID3D12InfoQueue::SetBreakOnID, direct3d12.id3d12infoqueue_setbreakonid
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.SetBreakOnID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12InfoQueue::SetBreakOnID


## -description


Set a message identifier to break on when a message with that identifier passes through the storage filter.




## -parameters




### -param ID [in]

Type: <b><a href="https://msdn.microsoft.com/95681EB0-C00B-42C8-91E1-1D1F657C886B">D3D12_MESSAGE_ID</a></b>

Message identifier to break on.
          


### -param bEnable [in]

Type: <b>BOOL</b>

Turns this breaking condition on or off (true for on, false for off).


          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>
 

 

