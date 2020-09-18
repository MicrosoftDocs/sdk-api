---
UID: NS:webservices._WS_CUSTOM_LISTENER_CALLBACKS
title: WS_CUSTOM_LISTENER_CALLBACKS (webservices.h)
description: A structure that is used to specify a set of callbacks that form the implementation of a custom listener.
helpviewer_keywords: ["WS_CUSTOM_LISTENER_CALLBACKS","WS_CUSTOM_LISTENER_CALLBACKS structure [Web Services for Windows]","webservices/WS_CUSTOM_LISTENER_CALLBACKS","wsw.ws_custom_listener_callbacks"]
old-location: wsw\ws_custom_listener_callbacks.htm
tech.root: wsw
ms.assetid: b0be530f-5eff-4daa-90be-f9be648dfad7
ms.date: 12/05/2018
ms.keywords: WS_CUSTOM_LISTENER_CALLBACKS, WS_CUSTOM_LISTENER_CALLBACKS structure [Web Services for Windows], webservices/WS_CUSTOM_LISTENER_CALLBACKS, wsw.ws_custom_listener_callbacks
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
req.typenames: WS_CUSTOM_LISTENER_CALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_CUSTOM_LISTENER_CALLBACKS
 - webservices/_WS_CUSTOM_LISTENER_CALLBACKS
 - WS_CUSTOM_LISTENER_CALLBACKS
 - webservices/WS_CUSTOM_LISTENER_CALLBACKS
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
 - WS_CUSTOM_LISTENER_CALLBACKS
---

# WS_CUSTOM_LISTENER_CALLBACKS structure


## -description

A structure that is used to specify a set of callbacks 
                that form the implementation of a custom
                listener.

## -struct-fields

### -field createListenerCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wscreatelistener">WsCreateListener</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_listener_callback">WS_CREATE_LISTENER_CALLBACK</a> for more information.

### -field freeListenerCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsfreelistener">WsFreeListener</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_free_listener_callback">WS_FREE_LISTENER_CALLBACK</a> for more information.

### -field resetListenerCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsresetlistener">WsResetListener</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_reset_listener_callback">WS_RESET_LISTENER_CALLBACK</a> for more information.

### -field openListenerCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsopenlistener">WsOpenListener</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_open_listener_callback">WS_OPEN_LISTENER_CALLBACK</a> for more information.

### -field closeListenerCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wscloselistener">WsCloseListener</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_close_listener_callback">WS_CLOSE_LISTENER_CALLBACK</a> for more information.

### -field abortListenerCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsabortlistener">WsAbortListener</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_abort_listener_callback">WS_ABORT_LISTENER_CALLBACK</a> for more information.

### -field getListenerPropertyCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsgetlistenerproperty">WsGetListenerProperty</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_get_listener_property_callback">WS_GET_LISTENER_PROPERTY_CALLBACK</a> for more information.

### -field setListenerPropertyCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wssetlistenerproperty">WsSetListenerProperty</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_set_listener_property_callback">WS_SET_LISTENER_PROPERTY_CALLBACK</a> for more information.

### -field createChannelForListenerCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannelforlistener">WsCreateChannelForListener</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_create_channel_for_listener_callback">WS_CREATE_CHANNEL_FOR_LISTENER_CALLBACK</a> for more information.

### -field acceptChannelCallback

The callback that implements <a href="/windows/desktop/api/webservices/nf-webservices-wsacceptchannel">WsAcceptChannel</a>.
                    See <a href="/windows/desktop/api/webservices/nc-webservices-ws_accept_channel_callback">WS_ACCEPT_CHANNEL_CALLBACK</a> for more information.

## -remarks

This structure is specified when a listener is created using
                <a href="/windows/desktop/api/webservices/nf-webservices-wscreatelistener">WsCreateListener</a> 
                using <a href="/windows/desktop/api/webservices/ne-webservices-ws_listener_property_id">WS_LISTENER_PROPERTY_CUSTOM_LISTENER_CALLBACKS</a>.
            

Except where noted, each callback is responsible for validating all parameters and
                that the operation requested is acceptable given the current
                <a href="/windows/desktop/api/webservices/ne-webservices-ws_listener_state">WS_LISTENER_STATE</a>.