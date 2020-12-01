---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnError
title: IXMLHTTPRequest2Callback::OnError (msxml6.h)
description: Occurs when an error is encountered or the request has been aborted.
helpviewer_keywords: ["IXMLHTTPRequest2Callback interface [XMLHttpRequest2]","OnError method","IXMLHTTPRequest2Callback.OnError","IXMLHTTPRequest2Callback::OnError","OnError","OnError method [XMLHttpRequest2]","OnError method [XMLHttpRequest2]","IXMLHTTPRequest2Callback interface","ixhr2.ixmlhttprequest2callback_onerror","msxml6/IXMLHTTPRequest2Callback::OnError"]
old-location: ixhr2\ixmlhttprequest2callback_onerror.htm
tech.root: ixhr2
ms.assetid: 532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2Callback interface [XMLHttpRequest2],OnError method, IXMLHTTPRequest2Callback.OnError, IXMLHTTPRequest2Callback::OnError, OnError, OnError method [XMLHttpRequest2], OnError method [XMLHttpRequest2],IXMLHTTPRequest2Callback interface, ixhr2.ixmlhttprequest2callback_onerror, msxml6/IXMLHTTPRequest2Callback::OnError
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
 - IXMLHTTPRequest2Callback::OnError
 - msxml6/IXMLHTTPRequest2Callback::OnError
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
 - IXMLHTTPRequest2Callback.OnError
---

# IXMLHTTPRequest2Callback::OnError


## -description

Occurs when an error is encountered or the request has been aborted.

## -parameters

### -param pXHR [in, optional]

The initial HTTP request.

### -param hrError

A code representing the error that occurred on the HTTP request.

## -returns

Returns<b> S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>

## -remarks

Unless the request completes successfully, indicated by <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onresponsereceived">OnResponseReceived</a>, the call to <b>OnError</b> is the final callback. The client should perform any required cleanup including releasing references to the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> object.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream Interface</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a>