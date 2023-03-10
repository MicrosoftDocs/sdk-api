---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetMessageCountLimit
title: ID3D11InfoQueue::SetMessageCountLimit (d3d11sdklayers.h)
description: Set the maximum number of messages that can be added to the message queue. (ID3D11InfoQueue.SetMessageCountLimit)
helpviewer_keywords: ["56bf62b4-6ca7-b852-eada-d18cbf109706","ID3D11InfoQueue interface [Direct3D 11]","SetMessageCountLimit method","ID3D11InfoQueue.SetMessageCountLimit","ID3D11InfoQueue::SetMessageCountLimit","SetMessageCountLimit","SetMessageCountLimit method [Direct3D 11]","SetMessageCountLimit method [Direct3D 11]","ID3D11InfoQueue interface","d3d11sdklayers/ID3D11InfoQueue::SetMessageCountLimit","direct3d11.id3d11infoqueue_setmessagecountlimit"]
old-location: direct3d11\id3d11infoqueue_setmessagecountlimit.htm
tech.root: direct3d11
ms.assetid: 59ed198c-65a5-4d78-867a-ba4527ad23c2
ms.date: 12/05/2018
ms.keywords: 56bf62b4-6ca7-b852-eada-d18cbf109706, ID3D11InfoQueue interface [Direct3D 11],SetMessageCountLimit method, ID3D11InfoQueue.SetMessageCountLimit, ID3D11InfoQueue::SetMessageCountLimit, SetMessageCountLimit, SetMessageCountLimit method [Direct3D 11], SetMessageCountLimit method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetMessageCountLimit, direct3d11.id3d11infoqueue_setmessagecountlimit
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
 - ID3D11InfoQueue::SetMessageCountLimit
 - d3d11sdklayers/ID3D11InfoQueue::SetMessageCountLimit
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
 - ID3D11InfoQueue.SetMessageCountLimit
---

# ID3D11InfoQueue::SetMessageCountLimit


## -description

Set the maximum number of messages that can be added to the message queue.

## -parameters

### -param MessageCountLimit [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Maximum number of messages that can be added to the message queue. -1 means no limit.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

When the number of messages in the message queue has reached the maximum limit, new messages coming in will push old messages out.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
