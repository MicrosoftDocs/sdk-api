---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.SetMessageCountLimit
title: ID3D12InfoQueue::SetMessageCountLimit (d3d12sdklayers.h)
description: Set the maximum number of messages that can be added to the message queue. (ID3D12InfoQueue.SetMessageCountLimit)
helpviewer_keywords: ["ID3D12InfoQueue interface","SetMessageCountLimit method","ID3D12InfoQueue.SetMessageCountLimit","ID3D12InfoQueue::SetMessageCountLimit","SetMessageCountLimit","SetMessageCountLimit method","SetMessageCountLimit method","ID3D12InfoQueue interface","d3d12sdklayers/ID3D12InfoQueue::SetMessageCountLimit","direct3d12.id3d12infoqueue_setmessagecountlimit"]
old-location: direct3d12\id3d12infoqueue_setmessagecountlimit.htm
tech.root: direct3d12
ms.assetid: A3C21C98-2B31-4901-8ED6-55E68507D200
ms.date: 12/05/2018
ms.keywords: ID3D12InfoQueue interface,SetMessageCountLimit method, ID3D12InfoQueue.SetMessageCountLimit, ID3D12InfoQueue::SetMessageCountLimit, SetMessageCountLimit, SetMessageCountLimit method, SetMessageCountLimit method,ID3D12InfoQueue interface, d3d12sdklayers/ID3D12InfoQueue::SetMessageCountLimit, direct3d12.id3d12infoqueue_setmessagecountlimit
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
 - ID3D12InfoQueue::SetMessageCountLimit
 - d3d12sdklayers/ID3D12InfoQueue::SetMessageCountLimit
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
 - ID3D12InfoQueue.SetMessageCountLimit
---

# ID3D12InfoQueue::SetMessageCountLimit


## -description

Set the maximum number of messages that can be added to the message queue.

## -parameters

### -param MessageCountLimit [in]

Type: <b>UINT64</b>

Maximum number of messages that can be added to the message queue. -1 means no limit.

When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
