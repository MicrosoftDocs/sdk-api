---
UID: NF:webservices.WsCloseChannel
title: WsCloseChannel function (webservices.h)
description: Closes a specified channel.
helpviewer_keywords: ["WsCloseChannel","WsCloseChannel function [Web Services for Windows]","webservices/WsCloseChannel","wsw.wsclosechannel"]
old-location: wsw\wsclosechannel.htm
tech.root: wsw
ms.assetid: e4928371-a172-4cc8-968b-12ae2ee2e0c6
ms.date: 12/05/2018
ms.keywords: WsCloseChannel, WsCloseChannel function [Web Services for Windows], webservices/WsCloseChannel, wsw.wsclosechannel
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
 - WsCloseChannel
 - webservices/WsCloseChannel
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
 - WsCloseChannel
---

# WsCloseChannel function


## -description

Closes a specified <a href="/windows/desktop/wsw/ws-channel">channel</a>.

## -parameters

### -param channel [in]

Pointer to a <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> structure representing the channel to close.

### -param asyncContext [in, optional]

Pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> data structure containing information for invoking the function asynchronously.  Pass a <b>NULL</b> 
                 value to call the function synchronously.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  where additional error information is stored if the function fails.

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
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The channel closure was aborted by a call to <a href="/windows/desktop/api/webservices/nf-webservices-wsabortchannel">WsAbortChannel</a> while the channel was closing.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The channel was in an inappropriate state (see the Remarks section).
                

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

If you open a channel or successfully accept a channel, you must close it when it is no longer needed. After a channel has been closed, the associated resources can safely be  freed.

The channel-closing process will wait for any already initiated, pending I/O to complete. 



If there are no messages currently being read or written for the channel, the channel attempts a graceful shutdown. Otherwise, all I/O still pending on the channel itself is aborted and the channel does a rude shutdown. 

If the channel attempts a graceful shutdown but encounters an error, <b>WsCloseChannel</b> will return an error, but the channel will still be closed. 



This operation is allowed only if the channel is in WS_CHANNEL_STATE_OPEN or WS_CHANNEL_STATE_FAULTED states.

Closing a channel automatically disassociates any messages that are in the
                process of being read or written. Therefore, it is not necessary to call 
                <a href="/windows/desktop/api/webservices/nf-webservices-wsabandonmessage">WsAbandonMessage</a> before calling <b>WsCloseChannel</b>).