---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.GetMessage
title: ID3D12InfoQueue::GetMessage (d3d12sdklayers.h)
description: Get a message from the message queue. (ID3D12InfoQueue.GetMessage)
helpviewer_keywords: ["GetMessage","GetMessage method","GetMessage method","ID3D12InfoQueue interface","ID3D12InfoQueue interface","GetMessage method","ID3D12InfoQueue.GetMessage","ID3D12InfoQueue::GetMessage","d3d12sdklayers/ID3D12InfoQueue::GetMessage","direct3d12.id3d12infoqueue_getmessage"]
old-location: direct3d12\id3d12infoqueue_getmessage.htm
tech.root: direct3d12
ms.assetid: B7B6D1C4-18FD-492A-8346-CA02FCD3EC4B
ms.date: 12/05/2018
ms.keywords: GetMessage, GetMessage method, GetMessage method,ID3D12InfoQueue interface, ID3D12InfoQueue interface,GetMessage method, ID3D12InfoQueue.GetMessage, ID3D12InfoQueue::GetMessage, d3d12sdklayers/ID3D12InfoQueue::GetMessage, direct3d12.id3d12infoqueue_getmessage
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
 - ID3D12InfoQueue::GetMessage
 - d3d12sdklayers/ID3D12InfoQueue::GetMessage
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
 - ID3D12InfoQueue.GetMessage
---

# ID3D12InfoQueue::GetMessage


## -description

Get a message from the message queue.

## -parameters

### -param MessageIndex [in]

Type: <b>UINT64</b>

Index into message queue after an optional retrieval filter has been applied. This can be between 0 and the number of messages in the message queue that pass through the retrieval filter (which can be obtained with <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getnumstoredmessagesallowedbyretrievalfilter">GetNumStoredMessagesAllowedByRetrievalFilter</a>). 0 is the message at the front of the message queue.

### -param pMessage [out, optional]

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message">D3D12_MESSAGE</a>*</b>

Returned message.

### -param pMessageByteLength [in, out]

Type: <b>SIZE_T*</b>

Size of <i>pMessage</i> in bytes.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

This method does not remove any messages from the message queue.



This method gets messages from the message queue after an optional retrieval filter has been applied.



Applications should call this method twice to retrieve a message - first to obtain the size of the message and second to get the message. Here is a typical example:




``` syntax
 
// Get the size of the message
SIZE_T messageLength = 0;
HRESULT hr = pInfoQueue->GetMessage(0, NULL, &messageLength);

// Allocate space and get the message
D3D12_MESSAGE * pMessage = (D3D12_MESSAGE*)malloc(messageLength);
hr = pInfoQueue->GetMessage(0, pMessage, &messageLength); 

```


## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue">ID3D12InfoQueue</a>
