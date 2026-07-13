---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
title: ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit (d3d11sdklayers.h)
description: Get the number of messages that were discarded due to the message count limit. (ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit)
helpviewer_keywords: ["GetNumMessagesDiscardedByMessageCountLimit","GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 11]","GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","GetNumMessagesDiscardedByMessageCountLimit method","ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit","ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit","d3d11sdklayers/ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit","direct3d11.id3d11infoqueue_getnummessagesdiscardedbymessagecountlimit","ef744f2d-3777-9d02-76c3-9279cdf0497b"]
old-location: direct3d11\id3d11infoqueue_getnummessagesdiscardedbymessagecountlimit.htm
tech.root: direct3d11
ms.assetid: 8a2cb3c3-2b8c-47bf-b306-e13f35729686
ms.date: 12/05/2018
ms.keywords: GetNumMessagesDiscardedByMessageCountLimit, GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 11], GetNumMessagesDiscardedByMessageCountLimit method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetNumMessagesDiscardedByMessageCountLimit method, ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit, ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit, d3d11sdklayers/ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit, direct3d11.id3d11infoqueue_getnummessagesdiscardedbymessagecountlimit, ef744f2d-3777-9d02-76c3-9279cdf0497b
req.header: d3d11sdklayers.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit
 - d3d11sdklayers/ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11InfoQueue.GetNumMessagesDiscardedByMessageCountLimit
---

# ID3D11InfoQueue::GetNumMessagesDiscardedByMessageCountLimit


## -description

Get the number of messages that were discarded due to the message count limit.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Number of messages discarded.

## -remarks

Get and set the message count limit with <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getmessagecountlimit">ID3D11InfoQueue::GetMessageCountLimit</a> and <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-setmessagecountlimit">ID3D11InfoQueue::SetMessageCountLimit</a>, respectively.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
