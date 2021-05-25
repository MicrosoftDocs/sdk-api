---
UID: NS:webservices._WS_CUSTOM_CHANNEL_CALLBACKS
title: WS_CUSTOM_CHANNEL_CALLBACKS (webservices.h)
description: A structure that is used to specify a set of callbacks that form the implementation of a custom channel.
helpviewer_keywords: ["WS_CUSTOM_CHANNEL_CALLBACKS","WS_CUSTOM_CHANNEL_CALLBACKS structure [Web Services for Windows]","webservices/WS_CUSTOM_CHANNEL_CALLBACKS","wsw.ws_custom_channel_callbacks"]
old-location: wsw\ws_custom_channel_callbacks.htm
tech.root: wsw
ms.assetid: 8df774fd-7cfc-4006-84ad-b81737770b6e
ms.date: 12/05/2018
ms.keywords: WS_CUSTOM_CHANNEL_CALLBACKS, WS_CUSTOM_CHANNEL_CALLBACKS structure [Web Services for Windows], webservices/WS_CUSTOM_CHANNEL_CALLBACKS, wsw.ws_custom_channel_callbacks
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
req.typenames: WS_CUSTOM_CHANNEL_CALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CUSTOM_CHANNEL_CALLBACKS
 - webservices/_WS_CUSTOM_CHANNEL_CALLBACKS
 - WS_CUSTOM_CHANNEL_CALLBACKS
 - webservices/WS_CUSTOM_CHANNEL_CALLBACKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CUSTOM_CHANNEL_CALLBACKS
---

# WS_CUSTOM_CHANNEL_CALLBACKS structure


## -description

A structure that is used to specify a set of callbacks
                that form the implementation of a custom channel.

## -struct-fields

### -field createChannelCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">WsCreateChannel</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_callback">WS_CREATE_CHANNEL_CALLBACK</a> for more information.

### -field freeChannelCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsfreechannel">WsFreeChannel</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_free_channel_callback">WS_FREE_CHANNEL_CALLBACK</a> for more information.

### -field resetChannelCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsresetchannel">WsResetChannel</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_reset_channel_callback">WS_RESET_CHANNEL_CALLBACK</a> for more information.

### -field openChannelCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsopenchannel">WsOpenChannel</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_open_channel_callback">WS_OPEN_CHANNEL_CALLBACK</a> for more information.

### -field closeChannelCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsclosechannel">WsCloseChannel</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_close_channel_callback">WS_CLOSE_CHANNEL_CALLBACK</a> for more information.

### -field abortChannelCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsabortchannel">WsAbortChannel</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_abort_channel_callback">WS_ABORT_CHANNEL_CALLBACK</a> for more information.

### -field getChannelPropertyCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsgetchannelproperty">WsGetChannelProperty</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_get_channel_property_callback">WS_GET_CHANNEL_PROPERTY_CALLBACK</a> for more information.

### -field setChannelPropertyCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wssetchannelproperty">WsSetChannelProperty</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_set_channel_property_callback">WS_SET_CHANNEL_PROPERTY_CALLBACK</a> for more information.

### -field writeMessageStartCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessagestart">WsWriteMessageStart</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_message_start_callback">WS_WRITE_MESSAGE_START_CALLBACK</a> for more information.

### -field writeMessageEndCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wswritemessageend">WsWriteMessageEnd</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_write_message_end_callback">WS_WRITE_MESSAGE_END_CALLBACK</a> for more information.

### -field readMessageStartCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessagestart">WsReadMessageStart</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_read_message_start_callback">WS_READ_MESSAGE_START_CALLBACK</a> for more information.

### -field readMessageEndCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmessageend">WsReadMessageEnd</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_read_message_end_callback">WS_READ_MESSAGE_END_CALLBACK</a> for more information.

### -field abandonMessageCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsabandonmessage">WsAbandonMessage</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_abandon_message_callback">WS_ABANDON_MESSAGE_CALLBACK</a> for more information.

### -field shutdownSessionChannelCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsshutdownsessionchannel">WsShutdownSessionChannel</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_shutdown_session_channel_callback">WS_SHUTDOWN_SESSION_CHANNEL_CALLBACK</a> for more information.

## -remarks

This structure is specified when a channel is created using
                <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">WsCreateChannel</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannelforlistener">WsCreateChannelForListener</a> using <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_CUSTOM_CHANNEL_CALLBACKS</a>.
            

Except where noted, each callback is responsible for validating all parameters and
                that the operation requested is acceptable given the current
                <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_state">WS_CHANNEL_STATE</a>.