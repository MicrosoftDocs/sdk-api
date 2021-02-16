---
UID: NF:msxml6.IXMLHTTPRequest2Callback.OnHeadersAvailable
title: IXMLHTTPRequest2Callback::OnHeadersAvailable (msxml6.h)
description: Occurs after an HTTP request has been sent to the server and the server has responded with response headers.
helpviewer_keywords: ["IXMLHTTPRequest2Callback interface [XMLHttpRequest2]","OnHeadersAvailable method","IXMLHTTPRequest2Callback.OnHeadersAvailable","IXMLHTTPRequest2Callback::OnHeadersAvailable","OnHeadersAvailable","OnHeadersAvailable method [XMLHttpRequest2]","OnHeadersAvailable method [XMLHttpRequest2]","IXMLHTTPRequest2Callback interface","ixhr2.ixmlhttprequest2callback_onheadersavailable","msxml6/IXMLHTTPRequest2Callback::OnHeadersAvailable"]
old-location: ixhr2\ixmlhttprequest2callback_onheadersavailable.htm
tech.root: ixhr2
ms.assetid: EB6580C5-B200-4281-BF1F-FA5C3220689E
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2Callback interface [XMLHttpRequest2],OnHeadersAvailable method, IXMLHTTPRequest2Callback.OnHeadersAvailable, IXMLHTTPRequest2Callback::OnHeadersAvailable, OnHeadersAvailable, OnHeadersAvailable method [XMLHttpRequest2], OnHeadersAvailable method [XMLHttpRequest2],IXMLHTTPRequest2Callback interface, ixhr2.ixmlhttprequest2callback_onheadersavailable, msxml6/IXMLHTTPRequest2Callback::OnHeadersAvailable
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
 - IXMLHTTPRequest2Callback::OnHeadersAvailable
 - msxml6/IXMLHTTPRequest2Callback::OnHeadersAvailable
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
 - IXMLHTTPRequest2Callback.OnHeadersAvailable
---

# IXMLHTTPRequest2Callback::OnHeadersAvailable


## -description

Occurs after an HTTP request has been sent to the server and the server has  responded with response headers.

## -parameters

### -param pXHR [in, optional]

The initial HTTP request object that returns the headers.

### -param dwStatus [in]

The status code for the request.

<div class="alert"><b>Note</b>  Possible values for this parameter also include the <b>HTTP_STATUS_*</b> values defined by <b>winhttp.h</b> for  desktop apps.</div>
<div> </div>

### -param pwszStatus [in]

The status code for the request appearing in human-readable form as a null-terminated string.

## -returns

Returns <b>S_OK</b> on success.

<div class="alert"><b>Note</b>  This callback function must not throw exceptions.</div>
<div> </div>

## -remarks

To view an individual response header, call the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getresponseheader">GetResponseHeader</a> method on the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> interface. To view all response headers, call the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getallresponseheaders">GetAllResponseHeaders</a> method. To cancel the request, call the Abort method On the pXHR object.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getallresponseheaders">GetAllResponseHeaders Method</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getresponseheader">GetResponseHeader Method</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable</a>