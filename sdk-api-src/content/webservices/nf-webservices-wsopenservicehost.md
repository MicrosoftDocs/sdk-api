---
UID: NF:webservices.WsOpenServiceHost
title: WsOpenServiceHost function (webservices.h)
description: Opens a Service Host for communication and starts the Listeners on all the endpoints. Client applications cannot connect to Service endpoints until WsOpenSerivceHost is called.
helpviewer_keywords: ["WsOpenServiceHost","WsOpenServiceHost function [Web Services for Windows]","webservices/WsOpenServiceHost","wsw.wsopenservicehost"]
old-location: wsw\wsopenservicehost.htm
tech.root: wsw
ms.assetid: 4e6ef553-7f0e-4ed7-bbdd-e85d4e0a095c
ms.date: 12/05/2018
ms.keywords: WsOpenServiceHost, WsOpenServiceHost function [Web Services for Windows], webservices/WsOpenServiceHost, wsw.wsopenservicehost
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
 - WsOpenServiceHost
 - webservices/WsOpenServiceHost
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
 - WsOpenServiceHost
---

# WsOpenServiceHost function


## -description

Opens a <a href="/windows/desktop/wsw/service-host">Service Host</a> for communication and starts the Listeners on all the endpoints. 
            Client applications cannot connect to Service endpoints until <b>WsOpenSerivceHost</b> is called.

## -parameters

### -param serviceHost [in]

A pointer to the <b>Service Host</b> object to open.  The pointer must reference a valid <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a> object
                    returned by <a href="/windows/desktop/api/webservices/nf-webservices-wscreateservicehost">WsCreateServiceHost</a> and the referenced <b>Service Host</b> value may not be <b>NULL</b>.

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
The service host was aborted before the open, or during the open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The current state of the service proxy is not valid for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ADDRESS_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The address is already being used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_ADDRESS_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The address is not valid for this context.

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

## -remarks

Note that all the endpoints listeners have to successfully open before any channel is accepted by service host for communicating 
                with the client.