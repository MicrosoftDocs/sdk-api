---
UID: NF:webservices.WsCloseServiceProxy
title: WsCloseServiceProxy function (webservices.h)
description: Closes down communication with the specified service proxy.
helpviewer_keywords: ["WsCloseServiceProxy","WsCloseServiceProxy function [Web Services for Windows]","webservices/WsCloseServiceProxy","wsw.wscloseserviceproxy"]
old-location: wsw\wscloseserviceproxy.htm
tech.root: wsw
ms.assetid: 034f9c60-5616-4ec7-9773-b34bde2e26c6
ms.date: 12/05/2018
ms.keywords: WsCloseServiceProxy, WsCloseServiceProxy function [Web Services for Windows], webservices/WsCloseServiceProxy, wsw.wscloseserviceproxy
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
 - WsCloseServiceProxy
 - webservices/WsCloseServiceProxy
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
 - WsCloseServiceProxy
---

# WsCloseServiceProxy function


## -description

Closes down communication with the specified <a href="/windows/desktop/wsw/service-proxy">service proxy</a>.

## -parameters

### -param serviceProxy [in]

Pointer to a <a href="/windows/desktop/wsw/ws-service-proxy">WS_SERVICE_PROXY</a> structure representing he service proxy to be closed.

### -param asyncContext [in, optional]

Pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> structure containing information for invoking the function asynchronously. Pass <b>NULL</b> to invoke the function synchronously.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The current state of the service proxy is not valid for this operation. This is only  
                   error for which close will fail. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ENDPOINT_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The underlying <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> was disconnected during the close operation. This error occurs only in cases where the underlying channel is session based.
                

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

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

## -remarks

If a service operation call is pending on the service proxy, <b>WsCloseServiceProxy</b> waits for each call to complete. After calling <b>WsCloseServiceProxy</b> application should not perform any more calls on the service proxy.
            

Note that WS_E_INVALID_OPERATION is the only  
                   error code that indicates that  closure has failed. Other error codes indicate that the operation succeeded, and the error code is for informational purposes only.