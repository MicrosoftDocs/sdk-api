---
UID: NF:dxgidebug.IDXGIInfoQueue.GetMessage
title: IDXGIInfoQueue::GetMessage (dxgidebug.h)
description: Gets a message from the message queue.
helpviewer_keywords: ["GetMessage","GetMessage method [DXGI]","GetMessage method [DXGI]","IDXGIInfoQueue interface","IDXGIInfoQueue interface [DXGI]","GetMessage method","IDXGIInfoQueue.GetMessage","IDXGIInfoQueue::GetMessage","direct3ddxgi.idxgiinfoqueue_getmessage","dxgidebug/IDXGIInfoQueue::GetMessage"]
old-location: direct3ddxgi\idxgiinfoqueue_getmessage.htm
tech.root: direct3ddxgi
ms.assetid: 208C3253-09AE-4379-808D-BA0BECC59BF8
ms.date: 12/05/2018
ms.keywords: GetMessage, GetMessage method [DXGI], GetMessage method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetMessage method, IDXGIInfoQueue.GetMessage, IDXGIInfoQueue::GetMessage, direct3ddxgi.idxgiinfoqueue_getmessage, dxgidebug/IDXGIInfoQueue::GetMessage
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: DXGIDebug.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIInfoQueue::GetMessage
 - dxgidebug/IDXGIInfoQueue::GetMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.GetMessage
---

# IDXGIInfoQueue::GetMessage


## -description

Gets a message from the message queue.

## -parameters

### -param Producer [in]

 A <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> value that identifies the entity that gets the message.

### -param MessageIndex [in]

An index into the message queue after an optional retrieval filter has been applied. This can be between 0 and the number of messages in the message queue that pass through the retrieval filter. Call <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getnumstoredmessagesallowedbyretrievalfilters">IDXGIInfoQueue::GetNumStoredMessagesAllowedByRetrievalFilters</a> to obtain this number. 0 is the message at the beginning of the message queue.

### -param pMessage [out, optional]

A pointer to a <a href="/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_message">DXGI_INFO_QUEUE_MESSAGE</a> structure that describes the message.

### -param pMessageByteLength [in, out]

A pointer to a variable that receives the size, in bytes, of the message description that <i>pMessage</i> points to. This size includes the size of the <a href="/windows/desktop/api/dxgidebug/ns-dxgidebug-dxgi_info_queue_message">DXGI_INFO_QUEUE_MESSAGE</a> structure in bytes.

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

This method doesn't remove any messages from the message queue.

This method gets a message from the message queue after an optional retrieval filter has been applied.

Call this method twice to retrieve a message, first to obtain the size of the message and second to get the message. Here is a typical example:


```

// Get the size of the message.
SIZE_T messageLength = 0;
HRESULT hr = pInfoQueue->GetMessage(DXGI_DEBUG_ALL, 0, NULL, &messageLength);
if(hr == S_FALSE){

    // Allocate space and get the message.
    DXGI_INFO_QUEUE_MESSAGE * pMessage = (DXGI_INFO_QUEUE_MESSAGE*)malloc(messageLength);
    hr = pInfoQueue->GetMessage(DXGI_DEBUG_ALL, 0, pMessage, &messageLength);
    
    // Do something with the message and free it
    if(hr == S_OK){
    
        // ...
        // ...
        // ...
        free(pMessage);
    }
}
```


<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a>
