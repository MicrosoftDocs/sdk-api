---
UID: NF:webservices.WsAbortServiceHost
title: WsAbortServiceHost function (webservices.h)
description: Aborts all current operations on the specified service host.
helpviewer_keywords: ["WsAbortServiceHost","WsAbortServiceHost function [Web Services for Windows]","webservices/WsAbortServiceHost","wsw.wsabortservicehost"]
old-location: wsw\wsabortservicehost.htm
tech.root: wsw
ms.assetid: d9405b21-52d2-4d33-b133-f15402dd1d5b
ms.date: 12/05/2018
ms.keywords: WsAbortServiceHost, WsAbortServiceHost function [Web Services for Windows], webservices/WsAbortServiceHost, wsw.wsabortservicehost
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
 - WsAbortServiceHost
 - webservices/WsAbortServiceHost
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
 - WsAbortServiceHost
---

# WsAbortServiceHost function


## -description

Aborts all current operations on the specified <a href="/windows/desktop/wsw/service-host">service host</a>.

## -parameters

### -param serviceHost [in]

Pointer to a <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a>  structure representing the service host on which to abort operations.

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

<b>WsAbortServiceHost</b> aborts all  listeners on the service host, and as a result, no new channels are accepted from the client. All channels currently being used by the service host to service messages are aborted as well. 

If a call is pending and it has a cancel callback registered through the <a href="/windows/desktop/api/webservices/nf-webservices-wsregisteroperationforcancel">WsRegisterOperationForCancel</a> function, the callback is called. However, the runtime still waits for the call to complete. 


           

For more information on registering for cancellation notification,
                see  <a href="/windows/desktop/api/webservices/nf-webservices-wsregisteroperationforcancel">WsRegisterOperationForCancel</a>.