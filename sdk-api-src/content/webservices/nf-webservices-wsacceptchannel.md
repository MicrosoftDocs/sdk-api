---
UID: NF:webservices.WsAcceptChannel
title: WsAcceptChannel function (webservices.h)
description: Accepts the next incoming message from the specified listener.
helpviewer_keywords: ["WsAcceptChannel","WsAcceptChannel function [Web Services for Windows]","webservices/WsAcceptChannel","wsw.wsacceptchannel"]
old-location: wsw\wsacceptchannel.htm
tech.root: wsw
ms.assetid: e18e0005-89bd-435e-9a12-6602c3c638b7
ms.date: 12/05/2018
ms.keywords: WsAcceptChannel, WsAcceptChannel function [Web Services for Windows], webservices/WsAcceptChannel, wsw.wsacceptchannel
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
 - WsAcceptChannel
 - webservices/WsAcceptChannel
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
 - WsAcceptChannel
---

# WsAcceptChannel function


## -description

Accepts the next incoming message from the specified <a href="/windows/desktop/wsw/listener">listener</a>.

## -parameters

### -param listener [in]

Pointer to a <a href="/windows/desktop/wsw/ws-listener">WS_LISTENER</a> structure representing the listener.
                This is the listener passed to <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannelforlistener">WsCreateChannelForListener</a> when the channel was created.

### -param channel [in]

Pointer to a <a href="/windows/desktop/wsw/ws-channel">WS_CHANNEL</a> structure representing the channel to accept.

### -param asyncContext [in, optional]

Pointer to a <a href="/windows/desktop/api/webservices/ns-webservices-ws_async_context">WS_ASYNC_CONTEXT</a> data structure with information for invoking the function asynchronously.  Pass a <b>NULL</b> 
                 value for a synchronous operation.

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
<dt><b>WS_E_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The listener or channel was aborted.
                
            

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OBJECT_FAULTED</b></dt>
</dl>
</td>
<td width="60%">
The listener has faulted. See the Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The listener or the channel or both were in an inappropriate state.
                
            See the Remarks section.

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
One or more arguments are  not valid.

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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>

## -remarks

Once you accept a channel, you must close it  when you no longer need it and free the resources by calling the  
                <a href="/windows/desktop/api/webservices/nf-webservices-wsclosechannel">WsCloseChannel</a> function, and then calling either the <a href="/windows/desktop/api/webservices/nf-webservices-wsfreechannel">WsFreeChannel</a> or the <a href="/windows/desktop/api/webservices/nf-webservices-wsresetchannel">WsResetChannel</a>.
            function. 

For <b>WsAcceptChannel</b> to succeed, the listener must be in WS_LISTENER_STATE_OPEN state, and the channel must be in WS_CHANNEL_STATE_CREATED state. For more information, see the <a href="/windows/desktop/api/webservices/ne-webservices-ws_listener_state">WS_LISTENER_STATE</a> and <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE</a> enumerations.

If a listener is in the <b>WS_LISTENER_STATE_FAULTED</b> state,  
                <b>WsAcceptChannel</b> immediately returns the <b>WS_E_OBJECT_FAULTED</b> error code. If an
                application is calling <b>WsAcceptChannel</b> in a loop, the application must check for this
                error, so it can end the loop.