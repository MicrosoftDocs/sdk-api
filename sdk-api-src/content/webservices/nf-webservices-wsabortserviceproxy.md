---
UID: NF:webservices.WsAbortServiceProxy
title: WsAbortServiceProxy function (webservices.h)
description: Aborts the service proxy, and cancels any pending I/O on the service proxy.
helpviewer_keywords: ["WsAbortServiceProxy","WsAbortServiceProxy function [Web Services for Windows]","webservices/WsAbortServiceProxy","wsw.wsabortserviceproxy"]
old-location: wsw\wsabortserviceproxy.htm
tech.root: wsw
ms.assetid: 45dc9df4-3a98-446f-b749-809607137fb1
ms.date: 12/05/2018
ms.keywords: WsAbortServiceProxy, WsAbortServiceProxy function [Web Services for Windows], webservices/WsAbortServiceProxy, wsw.wsabortserviceproxy
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
 - WsAbortServiceProxy
 - webservices/WsAbortServiceProxy
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
 - WsAbortServiceProxy
---

# WsAbortServiceProxy function


## -description

Aborts the <a href="/windows/desktop/wsw/service-proxy">service proxy</a>, and cancels any pending I/O on the service proxy.

## -parameters

### -param serviceProxy [in]

Pointer to a <a href="/windows/desktop/wsw/ws-service-proxy">WS_SERVICE_PROXY</a> structure representing the service proxy to abort.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure that receives additional error information if the function fails.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are invalid.

</td>
</tr>
</table>

## -remarks

<b>WsAbortServiceProxy</b> shows the following  behavior depending on the state of service proxy (see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_proxy_state">WS_SERVICE_PROXY_STATE</a> enumeration for possible states):<ul>
<li>If the service proxy is opening and in the WS_SERVICE_PROXY_STATE_OPENING state, you can call <b>WsAbortServiceProxy</b> to abort the opening operation. The service proxy will
                cancel all pending I/O and transition back to WS_SERVICE_PROXY_STATE_CREATED state.</li>
<li>If the service proxy is already open and in the WS_SERVICE_PROXY_STATE_OPEN state, <b>WsAbortServiceProxy</b> will cause the service proxy to abort all underlying channels and transition to the 
            WS_SERVICE_PROXY_STATE_FAULTED state. Once the abort is initiated, the service proxy will not accept any new calls. The application can call <a href="/windows/desktop/api/webservices/nf-webservices-wscloseserviceproxy">WsCloseServiceProxy</a> to close it</li>
<li>If the service proxy is closing and in the WS_SERVICE_PROXY_STATE_CLOSING state, all underlying channels are aborted, and the service proxy transitions to the WS_SERVICE_PROXY_STATE_CLOSED state. 
</li>
</ul>


For an example of using this function, see <a href="/windows/desktop/wsw/servicecancellationexample">ServiceCancellationExample</a>.