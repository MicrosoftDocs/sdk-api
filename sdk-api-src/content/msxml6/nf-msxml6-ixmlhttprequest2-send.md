---
UID: NF:msxml6.IXMLHTTPRequest2.Send
title: IXMLHTTPRequest2::Send (msxml6.h)
description: Sends an HTTP request to the server asynchronously. On success, methods on the IXMLHTTPRequest2Callback interface implemented by the app are called to process the response.
helpviewer_keywords: ["IXMLHTTPRequest2 interface [XMLHttpRequest2]","Send method","IXMLHTTPRequest2.Send","IXMLHTTPRequest2::Send","Send","Send method [XMLHttpRequest2]","Send method [XMLHttpRequest2]","IXMLHTTPRequest2 interface","ixhr2.ixmlhttprequest2_send","msxml6/IXMLHTTPRequest2::Send"]
old-location: ixhr2\ixmlhttprequest2_send.htm
tech.root: ixhr2
ms.assetid: E46DB550-8346-41F2-9B35-4DFD9732B0D8
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2 interface [XMLHttpRequest2],Send method, IXMLHTTPRequest2.Send, IXMLHTTPRequest2::Send, Send, Send method [XMLHttpRequest2], Send method [XMLHttpRequest2],IXMLHTTPRequest2 interface, ixhr2.ixmlhttprequest2_send, msxml6/IXMLHTTPRequest2::Send
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
 - IXMLHTTPRequest2::Send
 - msxml6/IXMLHTTPRequest2::Send
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
 - IXMLHTTPRequest2.Send
---

# IXMLHTTPRequest2::Send


## -description

Sends an HTTP request to the server asynchronously. On success, methods on the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a> interface implemented by the app are called to process the response.

## -parameters

### -param pBody [in, optional]

The body of the message being sent with the request. This stream is read in order to upload data for non-<b>GET</b> requests. For requests that do not require uploading, set this parameter to NULL.

### -param cbBody [in]

The length, in bytes, of the message being sent with the request. For requests that do not require uploading, set this parameter to 0.

## -returns

Returns <b>S_OK</b> on success.

## -remarks

The <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-open">Open</a> method must be called before <b>Send</b> can be called successfully.

Because this method is asynchronous, it returns immediately before the request has started processing.  The application will be notified through the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a> interface as progress is made in the request processing.

Alternatives to using <a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>  for a POST request include <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatememstream">SHCreateMemStream</a>/<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatestreamonfilea">SHCreateStreamOnFile</a> for desktop apps, and <a href="/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream">CreateStreamOverRandomAccessStream</a> for Windows Store apps.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>