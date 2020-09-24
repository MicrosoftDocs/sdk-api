---
UID: NF:webservices.WsOpenServiceProxy
title: WsOpenServiceProxy function (webservices.h)
description: Opens a Service Proxy to a Service endpoint.
helpviewer_keywords: ["WsOpenServiceProxy","WsOpenServiceProxy function [Web Services for Windows]","webservices/WsOpenServiceProxy","wsw.wsopenserviceproxy"]
old-location: wsw\wsopenserviceproxy.htm
tech.root: wsw
ms.assetid: b8a0afc7-2004-419d-8ab2-ce197c7e396d
ms.date: 12/05/2018
ms.keywords: WsOpenServiceProxy, WsOpenServiceProxy function [Web Services for Windows], webservices/WsOpenServiceProxy, wsw.wsopenserviceproxy
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
 - WsOpenServiceProxy
 - webservices/WsOpenServiceProxy
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
 - WsOpenServiceProxy
---

# WsOpenServiceProxy function


## -description

Opens a Service Proxy to a Service endpoint.
            

On success client applications can make calls using the Service Proxy. 
            The behavior of WsOpenServiceProxy is governed by the  <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">channel binding</a> used.

## -parameters

### -param serviceProxy [in]

A pointer to the <b>Service Proxy</b> to open.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-service-proxy">WS_SERVICE_PROXY</a> object
                    and the referenced value may not be <b>NULL</b>.

### -param address [in]

A pointer to the address of the endpoint.

### -param asyncContext [in, optional]

A pointer  to A WS_ASYNC_CONTEXT object that has information about how to invoke the function asynchronously.  The value is set to <b>NULL</b> if invoking synchronously.

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
<dt><b>WS_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The asynchronous operation is still pending.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

            

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

            

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint does not exist or could not be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access was denied by the remote endpoint.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The connection with the remote endpoint was terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint could not process the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint is not currently in service at this location.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_TOO_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint is unable to process the request due to being overloaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_UNREACHABLE</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint was not reachable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_ENDPOINT_URL</b></dt>
</dl>
</td>
<td width="60%">
The endpoint address URL is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OPERATION_TIMED_OUT</b></dt>
</dl>
</td>
<td width="60%">
The operation did not complete within the time allotted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access was denied by the HTTP proxy server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server could not process the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SECURITY_VERIFICATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Security verification was not successful for the received data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SECURITY_SYSTEM_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A security operation failed in the Windows Web Services framework.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_REQUIRES_BASIC_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server requires HTTP authentication scheme 'basic'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_REQUIRES_DIGEST_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server requires HTTP authentication scheme 'digest'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_REQUIRES_NEGOTIATE_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server requires HTTP authentication scheme 'negotiate'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_PROXY_REQUIRES_NTLM_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The HTTP proxy server requires HTTP authentication scheme 'NTLM'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SERVER_REQUIRES_BASIC_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint requires HTTP authentication scheme 'basic'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SERVER_REQUIRES_DIGEST_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint requires HTTP authentication scheme 'digest'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SERVER_REQUIRES_NEGOTIATE_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint requires HTTP authentication scheme 'negotiate'.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_SERVER_REQUIRES_NTLM_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The remote endpoint requires HTTP authentication scheme 'NTLM'.

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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>