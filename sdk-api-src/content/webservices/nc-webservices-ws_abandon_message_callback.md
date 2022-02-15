---
UID: NC:webservices.WS_ABANDON_MESSAGE_CALLBACK
title: WS_ABANDON_MESSAGE_CALLBACK (webservices.h)
description: Handles the WsAbandonMessage call for a WS_CUSTOM_CHANNEL_BINDING.
helpviewer_keywords: ["WS_ABANDON_MESSAGE_CALLBACK","WS_ABANDON_MESSAGE_CALLBACK callback","WS_ABANDON_MESSAGE_CALLBACK callback function [Web Services for Windows]","webservices/WS_ABANDON_MESSAGE_CALLBACK","wsw.ws_abandon_message_callback"]
old-location: wsw\ws_abandon_message_callback.htm
tech.root: wsw
ms.assetid: 494cfb49-c09e-4f51-85fd-5bb0f8d0a45d
ms.date: 12/05/2018
ms.keywords: WS_ABANDON_MESSAGE_CALLBACK, WS_ABANDON_MESSAGE_CALLBACK callback, WS_ABANDON_MESSAGE_CALLBACK callback function [Web Services for Windows], webservices/WS_ABANDON_MESSAGE_CALLBACK, wsw.ws_abandon_message_callback
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
 - WS_ABANDON_MESSAGE_CALLBACK
 - webservices/WS_ABANDON_MESSAGE_CALLBACK
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
 - WS_ABANDON_MESSAGE_CALLBACK
---

# WS_ABANDON_MESSAGE_CALLBACK callback function


## -description

Handles the <a href="/windows/desktop/api/webservices/nf-webservices-wsabandonmessage">WsAbandonMessage</a> call
                for a <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_CUSTOM_CHANNEL_BINDING</a>.

## -parameters

### -param channelInstance [in]

Pointer to the state specific to this channel instance,
                    as created by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_callback">WS_CREATE_CHANNEL_CALLBACK</a>.

### -param message [in]

The message that is current being read or written.  This should be
                    the same message as was passed to <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessagestart">WsWriteMessageStart</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a>.

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
This is returned if the channel is not in the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE_OPEN</a> state or the <b>WS_CHANNEL_STATE_FAULTED</b> state.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified message is not currently being read or written using the channel.
                

</td>
</tr>
</table>

## -remarks

See <a href="/windows/desktop/api/webservices/nf-webservices-wsabandonmessage">WsAbandonMessage</a> for information about the contract
                of this API.
