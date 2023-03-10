---
UID: NC:webservices.WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK
title: WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK (webservices.h)
description: Handles the WsShutdownSessionChannel call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK","WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback","WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback function [Web Services for Windows]","webservices/WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK","wsw.ws_shutdown_session_channel_callback"]
old-location: wsw\ws_shutdown_session_channel_callback.htm
tech.root: wsw
ms.assetid: 7dba0ae5-5610-4b8f-bbe5-b89244779e2d
ms.date: 12/05/2018
ms.keywords: WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK, WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback, WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback function [Web Services for Windows], webservices/WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK, wsw.ws_shutdown_session_channel_callback
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
 - WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK
 - webservices/WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK
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
 - WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK
---

# WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wsshutdownsessionchannel">WsShutdownSessionChannel</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param channelInstance [in]

The pointer to the state specific to this channel instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_callback">WS_CREATE_CHANNEL_CALLBACK</a>.

### -param asyncContext [in, optional]

Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.

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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
This is returned if the channel is not in the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE_OPEN</a> state.
                

</td>
</tr>
</table>

## -remarks

See <a href="/windows/desktop/api/webservices/nf-webservices-wsshutdownsessionchannel">WsShutdownSessionChannel</a> for information about the contract
                of this API.
