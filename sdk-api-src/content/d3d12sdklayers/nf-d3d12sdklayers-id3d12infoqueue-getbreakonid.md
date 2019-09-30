---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetBreakOnID
title: ID3D12InfoQueue::GetBreakOnID (d3d12sdklayers.h)
author: windows-sdk-content
description: Get a message identifier to break on when a message with that identifier passes through the storage filter.
old-location: direct3d12\id3d12infoqueue_getbreakonid.htm
tech.root: direct3d12
ms.assetid: 04763E09-3076-4865-8026-976ED08B61C3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBreakOnID, GetBreakOnID method, GetBreakOnID method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetBreakOnID method, ID3D12InfoQueue.GetBreakOnID, ID3D12InfoQueue::GetBreakOnID, d3d12sdklayers/ID3D12InfoQueue::GetBreakOnID, direct3d12.id3d12infoqueue_getbreakonid
ms.topic: method
f1_keywords: 
 - "d3d12sdklayers/ID3D12InfoQueue.GetBreakOnID"
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
 - ID3D12InfoQueue.GetBreakOnID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12InfoQueue::GetBreakOnID


## -description


Get a message identifier to break on when a message with that identifier passes through the storage filter.




## -parameters




### -param ID [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id">D3D12_MESSAGE_ID</a></b>

Message identifier to break on.
          


## -returns



Type: <b>BOOL</b>

Whether this breaking condition is turned on or off (true for on, false for off).






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
 

 

