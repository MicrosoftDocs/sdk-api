---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.GetMessage
title: ID3D11InfoQueue::GetMessage (d3d11sdklayers.h)
description: Get a message from the message queue. (ID3D11InfoQueue.GetMessage)
helpviewer_keywords: ["GetMessage","GetMessage method [Direct3D 11]","GetMessage method [Direct3D 11]","ID3D11InfoQueue interface","ID3D11InfoQueue interface [Direct3D 11]","GetMessage method","ID3D11InfoQueue.GetMessage","ID3D11InfoQueue::GetMessage","d3d11sdklayers/ID3D11InfoQueue::GetMessage","direct3d11.id3d11infoqueue_getmessage","fcb657d8-1742-cfff-a8cc-5af0bec46085"]
old-location: direct3d11\id3d11infoqueue_getmessage.htm
tech.root: direct3d11
ms.assetid: 685cddc5-cedd-410f-a693-665d2d69402e
ms.date: 12/05/2018
ms.keywords: GetMessage, GetMessage method [Direct3D 11], GetMessage method [Direct3D 11],ID3D11InfoQueue interface, ID3D11InfoQueue interface [Direct3D 11],GetMessage method, ID3D11InfoQueue.GetMessage, ID3D11InfoQueue::GetMessage, d3d11sdklayers/ID3D11InfoQueue::GetMessage, direct3d11.id3d11infoqueue_getmessage, fcb657d8-1742-cfff-a8cc-5af0bec46085
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
 - ID3D11InfoQueue::GetMessage
 - d3d11sdklayers/ID3D11InfoQueue::GetMessage
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
 - ID3D11InfoQueue.GetMessage
---

# ID3D11InfoQueue::GetMessage


## -description

Get a message from the message queue.

## -parameters

### -param MessageIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

Index into message queue after an optional retrieval filter has been applied. This can be between 0 and the number of messages in the message queue that pass through the retrieval filter (which can be obtained with <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11infoqueue-getnumstoredmessagesallowedbyretrievalfilter">ID3D11InfoQueue::GetNumStoredMessagesAllowedByRetrievalFilter</a>). 0 is the message at the front of the message queue.

### -param pMessage [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_message">D3D11_MESSAGE</a>*</b>

Returned message (see <a href="/windows/desktop/api/d3d11sdklayers/ns-d3d11sdklayers-d3d11_message">D3D11_MESSAGE</a>).

### -param pMessageByteLength [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a>*</b>

Size of pMessage in bytes, including the size of the message string that the pMessage points to.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

This method does not remove any messages from the message queue.

This method gets messages from the message queue after an optional retrieval filter has been applied.

Applications should call this method twice to retrieve a message - first to obtain the size of the message and second to get the message. Here is a typical example:


```

// Get the size of the message
SIZE_T messageLength = 0;
HRESULT hr = pInfoQueue->GetMessage(0, NULL, &messageLength);

// Allocate space and get the message
D3D11_MESSAGE * pMessage = (D3D11_MESSAGE*)malloc(messageLength);
hr = pInfoQueue->GetMessage(0, pMessage, &messageLength);

```


For an overview see <a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">Information Queue Overview</a>.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11infoqueue">ID3D11InfoQueue Interface</a>
