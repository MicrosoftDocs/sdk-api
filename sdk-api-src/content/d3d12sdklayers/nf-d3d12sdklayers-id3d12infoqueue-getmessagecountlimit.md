---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetMessageCountLimit
title: ID3D12InfoQueue::GetMessageCountLimit
author: windows-sdk-content
description: Get the maximum number of messages that can be added to the message queue.
old-location: direct3d12\id3d12infoqueue_getmessagecountlimit.htm
tech.root: direct3d12
ms.assetid: FAE16E2C-6E18-4345-88A8-DDC5836A75A9
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetMessageCountLimit, GetMessageCountLimit method, GetMessageCountLimit method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetMessageCountLimit method, ID3D12InfoQueue.GetMessageCountLimit, ID3D12InfoQueue::GetMessageCountLimit, d3d12sdklayers/ID3D12InfoQueue::GetMessageCountLimit, direct3d12.id3d12infoqueue_getmessagecountlimit
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
 - ID3D12InfoQueue.GetMessageCountLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12InfoQueue::GetMessageCountLimit


## -description


Get the maximum number of messages that can be added to the message queue.




## -parameters






## -returns



Type: <b>UINT64</b>

Maximum number of messages that can be added to the queue. -1 means no limit.

When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.






## -see-also




<a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>
 

 

