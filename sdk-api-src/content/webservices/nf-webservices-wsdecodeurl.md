---
UID: NF:webservices.WsDecodeUrl
title: WsDecodeUrl function (webservices.h)
description: Evaluates the components of an URL to determine its &quot;scheme&quot;.
helpviewer_keywords: ["DWsDecodeUrl","WsDecodeUrl","WsDecodeUrl function [Web Services for Windows]","webservices/WsDecodeUrl","wsw.wsdecodeurl"]
old-location: wsw\wsdecodeurl.htm
tech.root: wsw
ms.assetid: 67147b71-ca3a-4a17-a4f1-6ba608eca742
ms.date: 12/05/2018
ms.keywords: DWsDecodeUrl, WsDecodeUrl, WsDecodeUrl function [Web Services for Windows], webservices/WsDecodeUrl, wsw.wsdecodeurl
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsDecodeUrl
 - webservices/WsDecodeUrl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsDecodeUrl
---

# WsDecodeUrl function


## -description

Evaluates the components of an URL to determine its "scheme". A <a href="/windows/desktop/api/webservices/ne-webservices-ws_url_scheme_type">WS_URL_SCHEME_TYPE</a> value is encapsulated in a <a href="/windows/desktop/api/webservices/ns-webservices-ws_url">WS_URL</a> structure and a reference to the structure is returned via output parameter. 
                If the scheme is not recognized, the function returns WS_E_INVALID_FORMAT.    
                Only scheme types identified in  <b>WS_URL_SCHEME_TYPE</b> are supported.

## -parameters

### -param url [in]

A pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_string">WS_STRING</a>  representation of the URL to evaluate.

### -param flags [in]

Determines the URL scheme evaluation method.  See <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type">WS_URL_FLAGS</a>.

### -param heap [in]

A pointer to a <a href="/windows/desktop/wsw/ws-heap">WS_HEAP</a> in which to allocate the returned URL reference.

### -param outUrl

Reference to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_url">WS_URL</a> structure that encapsulates the <a href="/windows/desktop/api/webservices/ne-webservices-ws_url_scheme_type">WS_URL_SCHEME_TYPE</a> value.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input URL was not in the correct format, or the scheme was not recognized.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

The grammar parsed for the schemes "http", "https", "net.tcp" and "soap.udp" can be found at http://www.ietf.org/rfc/rfc3986.txt.  For these schemes:
                    <ul>
<li>A non-empty hostname is required.
                      </li>
<li>For the IP-literal production all the characters demarcated by "[" and "]" are returned.  They are not enforced to follow the IPv6Address production.
                    </li>
<li>The userinfo part of authority (for example, userinfo@hostname:port) is not supported.
                    </li>
</ul>


If no port is specified the default port for that scheme is returned.
            

If no port is specified for the soap.udp scheme 0xFFFFFFFF is returned as the default.