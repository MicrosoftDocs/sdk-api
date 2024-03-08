---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
title: ID3D10InfoQueue::GetNumMessagesDiscardedByMessageCountLimit (d3d10sdklayers.h)
description: Get the number of messages that were discarded due to the message count limit. (ID3D10InfoQueue.GetNumMessagesDiscardedByMessageCountLimit)
helpviewer_keywords: ["GetNumMessagesDiscardedByMessageCountLimit","GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 10]","GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","GetNumMessagesDiscardedByMessageCountLimit method","ID3D10InfoQueue.GetNumMessagesDiscardedByMessageCountLimit","ID3D10InfoQueue::GetNumMessagesDiscardedByMessageCountLimit","d12591c5-0fe7-d6c0-52b7-6344cee6e4a7","d3d10sdklayers/ID3D10InfoQueue::GetNumMessagesDiscardedByMessageCountLimit","direct3d10.id3d10infoqueue_getnummessagesdiscardedbymessagecountlimit"]
old-location: direct3d10\id3d10infoqueue_getnummessagesdiscardedbymessagecountlimit.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getnummessagesdiscardedbymessagecountlimit.htm
ms.date: 12/05/2018
ms.keywords: GetNumMessagesDiscardedByMessageCountLimit, GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 10], GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetNumMessagesDiscardedByMessageCountLimit method, ID3D10InfoQueue.GetNumMessagesDiscardedByMessageCountLimit, ID3D10InfoQueue::GetNumMessagesDiscardedByMessageCountLimit, d12591c5-0fe7-d6c0-52b7-6344cee6e4a7, d3d10sdklayers/ID3D10InfoQueue::GetNumMessagesDiscardedByMessageCountLimit, direct3d10.id3d10infoqueue_getnummessagesdiscardedbymessagecountlimit
req.header: d3d10sdklayers.h
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
 - ID3D10InfoQueue::GetNumMessagesDiscardedByMessageCountLimit
 - d3d10sdklayers/ID3D10InfoQueue::GetNumMessagesDiscardedByMessageCountLimit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
---

# ID3D10InfoQueue::GetNumMessagesDiscardedByMessageCountLimit


## -description

Get the number of messages that were discarded due to the message count limit.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of messages discarded.

## -remarks

Get and set the message count limit with <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-getmessagecountlimit">ID3D10InfoQueue::GetMessageCountLimit</a> and <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10infoqueue-setmessagecountlimit">ID3D10InfoQueue::SetMessageCountLimit</a>, respectively.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
