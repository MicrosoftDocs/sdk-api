---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnDataAvailable
title: IXMLHTTPRequest2Callback::OnDataAvailable (msxml6.h)
description: Occurs when a client receives part of the HTTP response data from the server.
helpviewer_keywords: ["IXMLHTTPRequest2Callback interface [XMLHttpRequest2]","OnDataAvailable method","IXMLHTTPRequest2Callback.OnDataAvailable","IXMLHTTPRequest2Callback::OnDataAvailable","OnDataAvailable","OnDataAvailable method [XMLHttpRequest2]","OnDataAvailable method [XMLHttpRequest2]","IXMLHTTPRequest2Callback interface","ixhr2.ixmlhttprequest2callback_ondataavailable","msxml6/IXMLHTTPRequest2Callback::OnDataAvailable"]
old-location: ixhr2\ixmlhttprequest2callback_ondataavailable.htm
tech.root: ixhr2
ms.assetid: 068C3288-A872-43FA-BF1F-D7A3CD2E2203
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2Callback interface [XMLHttpRequest2],OnDataAvailable method, IXMLHTTPRequest2Callback.OnDataAvailable, IXMLHTTPRequest2Callback::OnDataAvailable, OnDataAvailable, OnDataAvailable method [XMLHttpRequest2], OnDataAvailable method [XMLHttpRequest2],IXMLHTTPRequest2Callback interface, ixhr2.ixmlhttprequest2callback_ondataavailable, msxml6/IXMLHTTPRequest2Callback::OnDataAvailable
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
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
 - IXMLHTTPRequest2Callback::OnDataAvailable
 - msxml6/IXMLHTTPRequest2Callback::OnDataAvailable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2Callback.OnDataAvailable
---

# IXMLHTTPRequest2Callback::OnDataAvailable


## -description

Occurs when a client receives part of the HTTP response data from the server.

## -parameters

### -param pXHR [in, optional]

The initial HTTP request.

### -param pResponseStream [in, optional]

The response stream being received. The client can call <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> to begin processing the data, or it can wait until it has received the complete response. This response stream is wrapped in a stream synchronization object that prevents concurrent read and write operations, so the application does not need to implement custom synchronization.

## -returns

Returns <b>S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>

## -remarks

When this callback function returns  the application can begin processing data from the HTTP response, even if it has not yet received the entire response. However, receiving is suspended for the request until this callback function returns. Additionally, this callback can be  invoked multiple times during a single request.

This callback function must not block and should not be made to perform resource intensive operations such as UI updates.

Custom streams receive a call to <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> before <b>OnDataAvailable</b> is fired. The client can process data directly from the Write call instead of calling <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> on the custom stream, and it can rely on the Write call to indicate that new data is available.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream Interface</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a>