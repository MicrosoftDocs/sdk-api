---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetMessageCountLimit
title: ID3D11InfoQueue::GetMessageCountLimit (d3d11sdklayers.h)
description: Get the maximum number of messages that can be added to the message queue. (ID3D11InfoQueue.GetMessageCountLimit)
helpviewer_keywords: ["GetMessageCountLimit","GetMessageCountLimit method [Direct3D 11]","GetMessageCountLimit method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","GetMessageCountLimit method","ID3D11InfoQueue.GetMessageCountLimit","ID3D11InfoQueue::GetMessageCountLimit","d3d11sdklayers/ID3D11InfoQueue::GetMessageCountLimit","direct3d11.id3d11infoqueue_getmessagecountlimit","f8f0d99b-4472-147b-2074-368f1ee90957"]
old-location: direct3d11\id3d11infoqueue_getmessagecountlimit.htm
tech.root: direct3d11
ms.assetid: 971f3158-838d-4f1c-8d3c-15dac0b6dea9
ms.date: 12/05/2018
ms.keywords: GetMessageCountLimit, GetMessageCountLimit method [Direct3D 11], GetMessageCountLimit method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetMessageCountLimit method, ID3D11InfoQueue.GetMessageCountLimit, ID3D11InfoQueue::GetMessageCountLimit, d3d11sdklayers/ID3D11InfoQueue::GetMessageCountLimit, direct3d11.id3d11infoqueue_getmessagecountlimit, f8f0d99b-4472-147b-2074-368f1ee90957
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
 - ID3D11InfoQueue::GetMessageCountLimit
 - d3d11sdklayers/ID3D11InfoQueue::GetMessageCountLimit
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
 - ID3D11InfoQueue.GetMessageCountLimit
---

# ID3D11InfoQueue::GetMessageCountLimit


## -description

Get the maximum number of messages that can be added to the message queue.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Maximum number of messages that can be added to the queue. -1 means no limit.

## -remarks

When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
