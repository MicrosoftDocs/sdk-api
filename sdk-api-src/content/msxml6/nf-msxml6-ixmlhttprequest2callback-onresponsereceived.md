---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnResponseReceived
title: IXMLHTTPRequest2Callback::OnResponseReceived (msxml6.h)
description: Occurs when a client has received a complete response from the server.
helpviewer_keywords: ["IXMLHTTPRequest2Callback interface [XMLHttpRequest2]","OnResponseReceived method","IXMLHTTPRequest2Callback.OnResponseReceived","IXMLHTTPRequest2Callback::OnResponseReceived","OnResponseReceived","OnResponseReceived method [XMLHttpRequest2]","OnResponseReceived method [XMLHttpRequest2]","IXMLHTTPRequest2Callback interface","ixhr2.ixmlhttprequest2callback_onresponsereceived","msxml6/IXMLHTTPRequest2Callback::OnResponseReceived"]
old-location: ixhr2\ixmlhttprequest2callback_onresponsereceived.htm
tech.root: ixhr2
ms.assetid: 5D1D4D4B-CC49-4A63-A0D5-B29D618E80DE
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2Callback interface [XMLHttpRequest2],OnResponseReceived method, IXMLHTTPRequest2Callback.OnResponseReceived, IXMLHTTPRequest2Callback::OnResponseReceived, OnResponseReceived, OnResponseReceived method [XMLHttpRequest2], OnResponseReceived method [XMLHttpRequest2],IXMLHTTPRequest2Callback interface, ixhr2.ixmlhttprequest2callback_onresponsereceived, msxml6/IXMLHTTPRequest2Callback::OnResponseReceived
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
 - IXMLHTTPRequest2Callback::OnResponseReceived
 - msxml6/IXMLHTTPRequest2Callback::OnResponseReceived
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
 - IXMLHTTPRequest2Callback.OnResponseReceived
---

# IXMLHTTPRequest2Callback::OnResponseReceived


## -description

Occurs when a client has received a complete response from the server.

## -parameters

### -param pXHR [in, optional]

The initial HTTP request object

### -param pResponseStream [in, optional]

The response stream being received. The client can call <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> to begin processing the data, or it can store a reference to <i>pResponseStream</i> for later processing. This response stream is wrapped in a stream synchronization object that prevents concurrent read and write operations, so the application does not need to implement custom synchronization.

## -returns

Returns <b>S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>

## -remarks

When this event fires the application can begin processing data from the HTTP response. Processing may begin before this event fires if an earlier <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-ondataavailable">OnDataAvailable</a> event has occurred.

Unless <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onerror">OnError</a> is called, the call to <b>OnResponseReceived</b> is the final callback. The client should perform any required cleanup including releasing references to the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> object.

Custom streams receive a call to <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> specifying 0 bytes written before <b>OnResponseReceived</b> is fired. The client can process data directly from the Write call instead of calling <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> on the custom stream, and it can rely on the zero-byte Write call to indicate that the response has been received.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream Interface</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a>