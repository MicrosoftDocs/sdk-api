---
UID: NS:websocket._WEB_SOCKET_HTTP_HEADER
title: WEB_SOCKET_HTTP_HEADER (websocket.h)
description: Contains an HTTP header.
helpviewer_keywords: ["*PWEB_SOCKET_HTTP_HEADER","PWEB_SOCKET_HTTP_HEADER","PWEB_SOCKET_HTTP_HEADER structure pointer [Websocket Protocol Component API]","WEB_SOCKET_HTTP_HEADER","WEB_SOCKET_HTTP_HEADER structure [Websocket Protocol Component API]","websock.web_socket_http_header","websocket/PWEB_SOCKET_HTTP_HEADER","websocket/WEB_SOCKET_HTTP_HEADER"]
old-location: websock\web_socket_http_header.htm
tech.root: WebSock
ms.assetid: d051c2fd-c21c-43dc-9160-5626fb1d6d49
ms.date: 12/05/2018
ms.keywords: '*PWEB_SOCKET_HTTP_HEADER, PWEB_SOCKET_HTTP_HEADER, PWEB_SOCKET_HTTP_HEADER structure pointer [Websocket Protocol Component API], WEB_SOCKET_HTTP_HEADER, WEB_SOCKET_HTTP_HEADER structure [Websocket Protocol Component API], websock.web_socket_http_header, websocket/PWEB_SOCKET_HTTP_HEADER, websocket/WEB_SOCKET_HTTP_HEADER'
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
req.typenames: WEB_SOCKET_HTTP_HEADER, *PWEB_SOCKET_HTTP_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WEB_SOCKET_HTTP_HEADER
 - websocket/_WEB_SOCKET_HTTP_HEADER
 - PWEB_SOCKET_HTTP_HEADER
 - websocket/PWEB_SOCKET_HTTP_HEADER
 - WEB_SOCKET_HTTP_HEADER
 - websocket/WEB_SOCKET_HTTP_HEADER
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
 - WEB_SOCKET_HTTP_HEADER
---

# WEB_SOCKET_HTTP_HEADER structure


## -description

The <b>WEB_SOCKET_HTTP_HEADER</b> structure contains an HTTP header.

## -struct-fields

### -field pcName

Type: <b>PCHAR</b>

A pointer to the HTTP header name. The name must not  contain a colon character.

### -field ulNameLength

Type: <b>ULONG</b>

Length, in characters,  of the HTTP header pointed to by <b>pcName</b>.

### -field pcValue

Type: <b>PCHAR</b>

A pointer to the HTTP header value.

### -field ulValueLength

Type: <b>ULONG</b>

Length, in characters,  of the HTTP value pointed to by <b>pcValue</b>.

## -see-also

<a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginclienthandshake">WebSocketBeginClientHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginserverhandshake">WebSocketBeginServerHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketendclienthandshake">WebSocketEndClientHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketendserverhandshake">WebSocketEndServerHandshake</a>