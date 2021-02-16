---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnRedirect
title: IXMLHTTPRequest2Callback::OnRedirect (msxml6.h)
description: Occurs when a client sends an HTTP request that the server redirects to a new URL.
helpviewer_keywords: ["IXMLHTTPRequest2Callback interface [XMLHttpRequest2]","OnRedirect method","IXMLHTTPRequest2Callback.OnRedirect","IXMLHTTPRequest2Callback::OnRedirect","OnRedirect","OnRedirect method [XMLHttpRequest2]","OnRedirect method [XMLHttpRequest2]","IXMLHTTPRequest2Callback interface","ixhr2.ixmlhttprequest2callback_onredirect","msxml6/IXMLHTTPRequest2Callback::OnRedirect"]
old-location: ixhr2\ixmlhttprequest2callback_onredirect.htm
tech.root: ixhr2
ms.assetid: 8492FFD5-99C8-4545-B5FD-465CC01D0038
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2Callback interface [XMLHttpRequest2],OnRedirect method, IXMLHTTPRequest2Callback.OnRedirect, IXMLHTTPRequest2Callback::OnRedirect, OnRedirect, OnRedirect method [XMLHttpRequest2], OnRedirect method [XMLHttpRequest2],IXMLHTTPRequest2Callback interface, ixhr2.ixmlhttprequest2callback_onredirect, msxml6/IXMLHTTPRequest2Callback::OnRedirect
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
 - IXMLHTTPRequest2Callback::OnRedirect
 - msxml6/IXMLHTTPRequest2Callback::OnRedirect
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
 - IXMLHTTPRequest2Callback.OnRedirect
---

# IXMLHTTPRequest2Callback::OnRedirect


## -description

Occurs when a client sends an HTTP request that the server redirects to a new URL.

## -parameters

### -param pXHR [in, optional]

The HTTP request object being redirected.

### -param pwszRedirectUrl [in]

The new URL for the HTTP request.

## -returns

Returns <b>S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>

## -remarks

If the request redirection is not permitted, you can call the Abort method on the pXHR object.

XMLHTTPRequest2 imposes a maximum of 100 re-directions on any request. Any re-directions above that limit generate an <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onerror">OnError</a> event.
Applications have no access to the headers for re-directions.

Once the final redirection has completed and the final URL has been reached, the application receives an <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable</a> callback.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-abort">Abort Method</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onerror">OnError Event</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable Event</a>