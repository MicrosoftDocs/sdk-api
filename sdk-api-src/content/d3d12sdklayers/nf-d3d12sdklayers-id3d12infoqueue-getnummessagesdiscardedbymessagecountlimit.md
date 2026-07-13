---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
title: ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit (d3d12sdklayers.h)
description: Get the number of messages that were discarded due to the message count limit. (ID3D12InfoQueue.GetNumMessagesDiscardedByMessageCountLimit)
helpviewer_keywords: ["GetNumMessagesDiscardedByMessageCountLimit","GetNumMessagesDiscardedByMessageCountLimit method","GetNumMessagesDiscardedByMessageCountLimit method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","GetNumMessagesDiscardedByMessageCountLimit method","ID3D12InfoQueue.GetNumMessagesDiscardedByMessageCountLimit","ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit","d3d12sdklayers/ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit","direct3d12.id3d12infoqueue_getnummessagesdiscardedbymessagecountlimit"]
old-location: direct3d12\id3d12infoqueue_getnummessagesdiscardedbymessagecountlimit.htm
tech.root: direct3d12
ms.assetid: EB6C6D7F-7B28-4E5B-9E35-332A9D957102
ms.date: 12/05/2018
ms.keywords: GetNumMessagesDiscardedByMessageCountLimit, GetNumMessagesDiscardedByMessageCountLimit method, GetNumMessagesDiscardedByMessageCountLimit method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetNumMessagesDiscardedByMessageCountLimit method, ID3D12InfoQueue.GetNumMessagesDiscardedByMessageCountLimit, ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit, d3d12sdklayers/ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit, direct3d12.id3d12infoqueue_getnummessagesdiscardedbymessagecountlimit
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
 - ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit
 - d3d12sdklayers/ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit
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
 - ID3D12InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
---

# ID3D12InfoQueue::GetNumMessagesDiscardedByMessageCountLimit


## -description

Get the number of messages that were discarded due to the message count limit.



## -returns

Type: <b>UINT64</b>

Number of messages discarded.

## -remarks

Get and set the message count limit with <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessagecountlimit">GetMessageCountLimit</a> and <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-setmessagecountlimit">SetMessageCountLimit</a>, respectively.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
