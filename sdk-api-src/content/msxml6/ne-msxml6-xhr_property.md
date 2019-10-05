---
UID: NE:msxml6._XHR_PROPERTY
title: XHR_PROPERTY (msxml6.h)
author: windows-sdk-content
description: Defines properties that you can assign to an outgoing HTTP request by calling the SetProperty method.
old-location: ixhr2\xhr_property.htm
tech.root: ixhr2
ms.assetid: FE317413-F1A2-4FD7-9DB1-67410C912AF2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: XHR_PROPERTY, XHR_PROPERTY enumeration [XMLHttpRequest2], XHR_PROP_EXTENDED_ERROR, XHR_PROP_IGNORE_CERT_ERRORS, XHR_PROP_NO_AUTH, XHR_PROP_NO_CACHE, XHR_PROP_NO_CRED_PROMPT, XHR_PROP_NO_DEFAULT_HEADERS, XHR_PROP_QUERY_STRING_UTF8, XHR_PROP_REPORT_REDIRECT_STATUS, XHR_PROP_TIMEOUT, ixhr2.xhr_property, msxml6/XHR_PROPERTY, msxml6/XHR_PROP_EXTENDED_ERROR, msxml6/XHR_PROP_IGNORE_CERT_ERRORS, msxml6/XHR_PROP_NO_AUTH, msxml6/XHR_PROP_NO_CACHE, msxml6/XHR_PROP_NO_CRED_PROMPT, msxml6/XHR_PROP_NO_DEFAULT_HEADERS, msxml6/XHR_PROP_QUERY_STRING_UTF8, msxml6/XHR_PROP_REPORT_REDIRECT_STATUS, msxml6/XHR_PROP_TIMEOUT
ms.topic: enum
f1_keywords: 
 - "msxml6/XHR_PROPERTY"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msxml6.h
api_name:
 - XHR_PROPERTY
targetos: Windows
req.typenames: XHR_PROPERTY
req.redist: 
ms.custom: 19H1
---

# XHR_PROPERTY enumeration


## -description


Defines properties that you can assign to an outgoing HTTP request by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a> method.


## -enum-fields




### -field XHR_PROP_NO_CRED_PROMPT

Sets a flag in the HTTP request that suppresses automatic prompts for credentials.


### -field XHR_PROP_NO_AUTH

Sets a flag in the HTTP request that configures the HTTP request that disables authentication for the request.


### -field XHR_PROP_TIMEOUT

Sets the connect, send, and receive timeouts for HTTP socket operations.

<div class="alert"><b>Note</b>  This value will not affect the timeout behavior of the entire request process.</div>
<div> </div>

### -field XHR_PROP_NO_DEFAULT_HEADERS

Suppresses adding default headers to the HTTP request.


### -field XHR_PROP_REPORT_REDIRECT_STATUS

Causes the HTTP stack to call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable</a> callback method with an interim redirecting status code.  The <b>OnHeadersAvailable</b> will be called again for additional redirects and the final destination status code.


### -field XHR_PROP_NO_CACHE

Suppresses cache reads and writes for the HTTP request.


### -field XHR_PROP_EXTENDED_ERROR

Causes the HTTP stack to provide <b>HRESULTS</b> with the underlying Win32 error code to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onerror">OnError</a> callback method in case of failure.


### -field XHR_PROP_QUERY_STRING_UTF8

Causes the query string to be encoded in UTF8 instead of ACP for HTTP request.


### -field XHR_PROP_IGNORE_CERT_ERRORS

Suppresses certain certificate errors.


### -field XHR_PROP_ONDATA_THRESHOLD


### -field XHR_PROP_SET_ENTERPRISEID


### -field XHR_PROP_MAX_CONNECTIONS




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onerror">OnError</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>
 

 

