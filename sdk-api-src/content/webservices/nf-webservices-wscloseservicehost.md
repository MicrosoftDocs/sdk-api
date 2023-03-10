---
UID: NF:webservices.WsCloseServiceHost
title: WsCloseServiceHost function (webservices.h)
description: Closes down communication with the specified service host.
helpviewer_keywords: ["WsCloseServiceHost","WsCloseServiceHost function [Web Services for Windows]","webservices/WsCloseServiceHost","wsw.wscloseservicehost"]
old-location: wsw\wscloseservicehost.htm
tech.root: wsw
ms.assetid: 46abbcba-72ba-4328-858d-367218f45df3
ms.date: 12/05/2018
ms.keywords: WsCloseServiceHost, WsCloseServiceHost function [Web Services for Windows], webservices/WsCloseServiceHost, wsw.wscloseservicehost
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WsCloseServiceHost
 - webservices/WsCloseServiceHost
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
 - WsCloseServiceHost
---

# WsCloseServiceHost function


## -description

Closes down communication with the specified <a href="/windows/desktop/wsw/service-host">service host</a>.

## -parameters

### -param serviceHost [in]

Pointer to a <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a> structure that represents the service host to be closed.

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
The current state of the service host is not valid for this operation.

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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

<b>WsCloseServiceHost</b> closes all  listeners on the service host. As a result, no new 
                channels are accepted from the client. However, pending I/O on  channels already accepted 
                is allowed to complete. 
                

This has implications for endpoints configured to run with session-based channel bindings. If a client has an open session with a service on such an endpoint, the 
                closure will not complete until the client closes the session with the service.