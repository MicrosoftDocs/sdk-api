---
UID: NE:msxml6._XHR_PROPERTY
title: "_XHR_PROPERTY"
author: windows-driver-content
description: Defines properties that you can assign to an outgoing HTTP request by calling the SetProperty method.
old-location: ixhr2\xhr_property.htm
old-project: ixhr2
ms.assetid: FE317413-F1A2-4FD7-9DB1-67410C912AF2
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: XHR_PROPERTY, XHR_PROPERTY enumeration [XMLHttpRequest2], XHR_PROP_EXTENDED_ERROR, XHR_PROP_IGNORE_CERT_ERRORS, XHR_PROP_NO_AUTH, XHR_PROP_NO_CACHE, XHR_PROP_NO_CRED_PROMPT, XHR_PROP_NO_DEFAULT_HEADERS, XHR_PROP_QUERY_STRING_UTF8, XHR_PROP_REPORT_REDIRECT_STATUS, XHR_PROP_TIMEOUT, _XHR_PROPERTY, ixhr2.xhr_property, msxml6/XHR_PROPERTY, msxml6/XHR_PROP_EXTENDED_ERROR, msxml6/XHR_PROP_IGNORE_CERT_ERRORS, msxml6/XHR_PROP_NO_AUTH, msxml6/XHR_PROP_NO_CACHE, msxml6/XHR_PROP_NO_CRED_PROMPT, msxml6/XHR_PROP_NO_DEFAULT_HEADERS, msxml6/XHR_PROP_QUERY_STRING_UTF8, msxml6/XHR_PROP_REPORT_REDIRECT_STATUS, msxml6/XHR_PROP_TIMEOUT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Msxml.tlb
req.typenames: XHR_PROPERTY, XHR_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	msxml6.h
api_name:
-	XHR_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: Msxml.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _XHR_PROPERTY enumeration


## -description


Defines properties that you can assign to an outgoing HTTP request by calling the <a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a> method.


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

Causes the HTTP stack to call the <a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a> callback method with an interim redirecting status code.  The <b>OnHeadersAvailable</b> will be called again for additional redirects and the final destination status code.


### -field XHR_PROP_NO_CACHE

Suppresses cache reads and writes for the HTTP request.


### -field XHR_PROP_EXTENDED_ERROR

Causes the HTTP stack to provide <b>HRESULTS</b> with the underlying Win32 error code to the <a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">OnError</a> callback method in case of failure.


### -field XHR_PROP_QUERY_STRING_UTF8

Causes the query string to be encoded in UTF8 instead of ACP for HTTP request.


### -field XHR_PROP_IGNORE_CERT_ERRORS

Suppresses certain certificate errors.


### -field XHR_PROP_ONDATA_THRESHOLD


### -field XHR_PROP_SET_ENTERPRISEID


### -field XHR_PROP_MAX_CONNECTIONS




## -see-also




<a href="https://msdn.microsoft.com/532C97A7-B952-47BE-A9C7-5B1E5AB4C3D3">OnError</a>



<a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 

