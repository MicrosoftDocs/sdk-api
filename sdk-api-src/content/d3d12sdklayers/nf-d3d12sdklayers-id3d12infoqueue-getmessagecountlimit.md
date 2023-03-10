---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetMessageCountLimit
title: ID3D12InfoQueue::GetMessageCountLimit (d3d12sdklayers.h)
description: Get the maximum number of messages that can be added to the message queue. (ID3D12InfoQueue.GetMessageCountLimit)
helpviewer_keywords: ["GetMessageCountLimit","GetMessageCountLimit method","GetMessageCountLimit method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","GetMessageCountLimit method","ID3D12InfoQueue.GetMessageCountLimit","ID3D12InfoQueue::GetMessageCountLimit","d3d12sdklayers/ID3D12InfoQueue::GetMessageCountLimit","direct3d12.id3d12infoqueue_getmessagecountlimit"]
old-location: direct3d12\id3d12infoqueue_getmessagecountlimit.htm
tech.root: direct3d12
ms.assetid: FAE16E2C-6E18-4345-88A8-DDC5836A75A9
ms.date: 12/05/2018
ms.keywords: GetMessageCountLimit, GetMessageCountLimit method, GetMessageCountLimit method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetMessageCountLimit method, ID3D12InfoQueue.GetMessageCountLimit, ID3D12InfoQueue::GetMessageCountLimit, d3d12sdklayers/ID3D12InfoQueue::GetMessageCountLimit, direct3d12.id3d12infoqueue_getmessagecountlimit
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
 - ID3D12InfoQueue::GetMessageCountLimit
 - d3d12sdklayers/ID3D12InfoQueue::GetMessageCountLimit
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
 - ID3D12InfoQueue.GetMessageCountLimit
---

# ID3D12InfoQueue::GetMessageCountLimit


## -description

Get the maximum number of messages that can be added to the message queue.



## -returns

Type: <b>UINT64</b>

Maximum number of messages that can be added to the queue. -1 means no limit.

When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
