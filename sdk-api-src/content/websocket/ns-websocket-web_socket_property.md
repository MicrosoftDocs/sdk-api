---
UID: NS:websocket._WEB_SOCKET_PROPERTY
title: WEB_SOCKET_PROPERTY (websocket.h)
description: Contains a single WebSocket property.
helpviewer_keywords: ["*PWEB_SOCKET_PROPERTY","PWEB_SOCKET_PROPERTY","PWEB_SOCKET_PROPERTY structure pointer [Websocket Protocol Component API]","WEB_SOCKET_PROPERTY","WEB_SOCKET_PROPERTY structure [Websocket Protocol Component API]","websock.web_socket_property","websocket/PWEB_SOCKET_PROPERTY","websocket/WEB_SOCKET_PROPERTY"]
old-location: websock\web_socket_property.htm
tech.root: WebSock
ms.assetid: c8b35288-4cc1-4839-a5be-4fd13b162c20
ms.date: 12/05/2018
ms.keywords: '*PWEB_SOCKET_PROPERTY, PWEB_SOCKET_PROPERTY, PWEB_SOCKET_PROPERTY structure pointer [Websocket Protocol Component API], WEB_SOCKET_PROPERTY, WEB_SOCKET_PROPERTY structure [Websocket Protocol Component API], websock.web_socket_property, websocket/PWEB_SOCKET_PROPERTY, websocket/WEB_SOCKET_PROPERTY'
req.header: websocket.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WEB_SOCKET_PROPERTY
 - websocket/_WEB_SOCKET_PROPERTY
 - PWEB_SOCKET_PROPERTY
 - websocket/PWEB_SOCKET_PROPERTY
 - WEB_SOCKET_PROPERTY
 - websocket/WEB_SOCKET_PROPERTY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Websocket.h
api_name:
 - WEB_SOCKET_PROPERTY
---

# WEB_SOCKET_PROPERTY structure


## -description

The <b>WEB_SOCKET_PROPERTY</b> structure contains a  single WebSocket property.

## -struct-fields

### -field Type

Type: <b><a href="/windows/desktop/api/websocket/ne-websocket-web_socket_property_type">WEB_SOCKET_PROPERTY_TYPE</a></b>

The WebSocket property type.

### -field pvValue

Type: <b>PVOID</b>

A pointer to the value to set. The pointer must have an alignment compatible with the type of the property.

### -field ulValueSize

Type: <b>ULONG</b>

The size, in bytes, of the property pointed to by <b>pvValue</b>.

## -see-also

<a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a>