---
UID: NE:webservices.__unnamed_enum_19
title: WS_CHANNEL_TYPE (webservices.h)
description: Indicates the basic characteristics of the channel, such as whether it is sessionful, and what directions of communication are supported.
helpviewer_keywords: ["WS_CHANNEL_TYPE","WS_CHANNEL_TYPE enumeration [Web Services for Windows]","WS_CHANNEL_TYPE_DUPLEX","WS_CHANNEL_TYPE_DUPLEX_SESSION","WS_CHANNEL_TYPE_INPUT","WS_CHANNEL_TYPE_INPUT_SESSION","WS_CHANNEL_TYPE_OUTPUT","WS_CHANNEL_TYPE_OUTPUT_SESSION","WS_CHANNEL_TYPE_REPLY","WS_CHANNEL_TYPE_REQUEST","WS_CHANNEL_TYPE_SESSION","webservices/WS_CHANNEL_TYPE","webservices/WS_CHANNEL_TYPE_DUPLEX","webservices/WS_CHANNEL_TYPE_DUPLEX_SESSION","webservices/WS_CHANNEL_TYPE_INPUT","webservices/WS_CHANNEL_TYPE_INPUT_SESSION","webservices/WS_CHANNEL_TYPE_OUTPUT","webservices/WS_CHANNEL_TYPE_OUTPUT_SESSION","webservices/WS_CHANNEL_TYPE_REPLY","webservices/WS_CHANNEL_TYPE_REQUEST","webservices/WS_CHANNEL_TYPE_SESSION","wsw.ws_channel_type"]
old-location: wsw\ws_channel_type.htm
tech.root: wsw
ms.assetid: 7e1092f9-10e8-485c-a286-770e1c74d8ca
ms.date: 12/05/2018
ms.keywords: WS_CHANNEL_TYPE, WS_CHANNEL_TYPE enumeration [Web Services for Windows], WS_CHANNEL_TYPE_DUPLEX, WS_CHANNEL_TYPE_DUPLEX_SESSION, WS_CHANNEL_TYPE_INPUT, WS_CHANNEL_TYPE_INPUT_SESSION, WS_CHANNEL_TYPE_OUTPUT, WS_CHANNEL_TYPE_OUTPUT_SESSION, WS_CHANNEL_TYPE_REPLY, WS_CHANNEL_TYPE_REQUEST, WS_CHANNEL_TYPE_SESSION, webservices/WS_CHANNEL_TYPE, webservices/WS_CHANNEL_TYPE_DUPLEX, webservices/WS_CHANNEL_TYPE_DUPLEX_SESSION, webservices/WS_CHANNEL_TYPE_INPUT, webservices/WS_CHANNEL_TYPE_INPUT_SESSION, webservices/WS_CHANNEL_TYPE_OUTPUT, webservices/WS_CHANNEL_TYPE_OUTPUT_SESSION, webservices/WS_CHANNEL_TYPE_REPLY, webservices/WS_CHANNEL_TYPE_REQUEST, webservices/WS_CHANNEL_TYPE_SESSION, wsw.ws_channel_type
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WS_CHANNEL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_CHANNEL_TYPE
 - webservices/WS_CHANNEL_TYPE
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
 - WS_CHANNEL_TYPE
---

# WS_CHANNEL_TYPE enumeration


## -description

Indicates the basic characteristics of the channel, such as whether it is
                sessionful, and what directions of communication are supported.

## -enum-fields

### -field WS_CHANNEL_TYPE_INPUT:0x1

Input channels support Receive operations.  They are used on the sender side.
                

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_UDP_CHANNEL_BINDING</a> supports this channel type
                    when used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannelforlistener">WsCreateChannelForListener</a>.

### -field WS_CHANNEL_TYPE_OUTPUT:0x2

Output channels support Send operations.
                

This channel type is not currently supported by any channel bindings.

### -field WS_CHANNEL_TYPE_SESSION:0x4

Sessionful channels provide channel-level correlation of all messages sent or received.
                

This is a flag used to build <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_type">WS_CHANNEL_TYPE_INPUT_SESSION</a>,
                    <b>WS_CHANNEL_TYPE_OUTPUT_SESSION</b>, and <b>WS_CHANNEL_TYPE_DUPLEX_SESSION</b>,
                    but cannot be used alone.

### -field WS_CHANNEL_TYPE_INPUT_SESSION

An input channel that supports a session.
                

This channel type is not currently supported by any channel bindings.

### -field WS_CHANNEL_TYPE_OUTPUT_SESSION

An output channel that supports a session.
                

This channel type is not currently supported by any channel bindings.

### -field WS_CHANNEL_TYPE_DUPLEX

An input/output channel.
                

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_UDP_CHANNEL_BINDING</a> supports this channel type
                    when used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">WsCreateChannel</a>.

### -field WS_CHANNEL_TYPE_DUPLEX_SESSION

An input/output channel that supports a session.
                

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_TCP_CHANNEL_BINDING</a> supports this channel type when
                    used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">WsCreateChannel</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannelforlistener">WsCreateChannelForListener</a>.

### -field WS_CHANNEL_TYPE_REQUEST:0x8

Request channels support Send followed by Receive.  They are used on the client 
                    side for channels that support request-reply operations.
                

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a> supports this channel type when
                    used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannel">WsCreateChannel</a>.
                

Note that request channels provide built-in correlation of request replies.
                    It is possible to do request-reply correlation on other channel types using the
                    addressing headers (RelatesTo and MessageID).

### -field WS_CHANNEL_TYPE_REPLY:0x10

Reply channels support Receive followed by Send.  They are used on the service
                    side for channels that support request-reply operations (for example, HTTP).
                

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a> supports this channel type when
                    used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreatechannelforlistener">WsCreateChannelForListener</a>.
                

Note that reply channels provide built-in correlation of request replies.
                    It is possible to do request-reply correlation on other channel types using the
                    addressing headers (RelatesTo and MessageID).
