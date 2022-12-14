---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.GetMessageCountLimit
title: ID3D10InfoQueue::GetMessageCountLimit (d3d10sdklayers.h)
description: Get the maximum number of messages that can be added to the message queue. (ID3D10InfoQueue.GetMessageCountLimit)
helpviewer_keywords: ["GetMessageCountLimit","GetMessageCountLimit method [Direct3D 10]","GetMessageCountLimit method [Direct3D 10]","ID3D10InfoQueue interface","ID3D10InfoQueue interface [Direct3D 10]","GetMessageCountLimit method","ID3D10InfoQueue.GetMessageCountLimit","ID3D10InfoQueue::GetMessageCountLimit","bf741d73-e29b-2506-211e-4de8244d540a","d3d10sdklayers/ID3D10InfoQueue::GetMessageCountLimit","direct3d10.id3d10infoqueue_getmessagecountlimit"]
old-location: direct3d10\id3d10infoqueue_getmessagecountlimit.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_getmessagecountlimit.htm
ms.date: 12/05/2018
ms.keywords: GetMessageCountLimit, GetMessageCountLimit method [Direct3D 10], GetMessageCountLimit method [Direct3D 10],ID3D10InfoQueue interface, ID3D10InfoQueue interface [Direct3D 10],GetMessageCountLimit method, ID3D10InfoQueue.GetMessageCountLimit, ID3D10InfoQueue::GetMessageCountLimit, bf741d73-e29b-2506-211e-4de8244d540a, d3d10sdklayers/ID3D10InfoQueue::GetMessageCountLimit, direct3d10.id3d10infoqueue_getmessagecountlimit
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
 - ID3D10InfoQueue::GetMessageCountLimit
 - d3d10sdklayers/ID3D10InfoQueue::GetMessageCountLimit
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
 - ID3D10InfoQueue.GetMessageCountLimit
---

# ID3D10InfoQueue::GetMessageCountLimit


## -description

Get the maximum number of messages that can be added to the message queue.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Maximum number of messages that can be added to the queue. -1 means no limit.

## -remarks

When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10infoqueue">ID3D10InfoQueue Interface</a>
