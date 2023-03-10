---
UID: NC:webservices.WS_ACCEPT_CHANNEL_CALLBACK
title: WS_ACCEPT_CHANNEL_CALLBACK (webservices.h)
description: Handles the WsAcceptChannel call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_ACCEPT_CHANNEL_CALLBACK","WS_ACCEPT_CHANNEL_CALLBACK callback","WS_ACCEPT_CHANNEL_CALLBACK callback function [Web Services for Windows]","webservices/WS_ACCEPT_CHANNEL_CALLBACK","wsw.ws_accept_channel_callback"]
old-location: wsw\ws_accept_channel_callback.htm
tech.root: wsw
ms.assetid: 2c7f36cf-ee7d-4de0-8599-ccfd066cca7e
ms.date: 12/05/2018
ms.keywords: WS_ACCEPT_CHANNEL_CALLBACK, WS_ACCEPT_CHANNEL_CALLBACK callback, WS_ACCEPT_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_ACCEPT_CHANNEL_CALLBACK, wsw.ws_accept_channel_callback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_ACCEPT_CHANNEL_CALLBACK
 - webservices/WS_ACCEPT_CHANNEL_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_ACCEPT_CHANNEL_CALLBACK
---

# WS_ACCEPT_CHANNEL_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wsacceptchannel">WsAcceptChannel</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param listenerInstance [in]

The pointer to the state specific to this listener instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_listener_callback">WS_CREATE_LISTENER_CALLBACK</a>.

### -param channelInstance [in]

The pointer to the state specific to the channel instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_callback">WS_CREATE_CHANNEL_CALLBACK</a> when <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannelforlistener">WsCreateChannelForListener</a> was called.

### -param asyncContext [in, optional]

Information on how to invoke the function asynchronously, or NULL if invoking synchronously.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

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
The listener and/or channel was aborted.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_OBJECT_FAULTED</b></dt>
</dl>
</td>
<td width="60%">
The listener has faulted.  Once a listener has faulted,
                    then accepts will immediately return this error.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The listener was in an inappropriate state.
                

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

See <a href="/windows/desktop/api/webservices/nf-webservices-wsacceptchannel">WsAcceptChannel</a> for information about the contract
                of this API.
