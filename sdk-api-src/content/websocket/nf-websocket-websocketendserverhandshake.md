---
UID: NF:websocket.WebSocketEndServerHandshake
title: WebSocketEndServerHandshake function (websocket.h)
description: Completes the server-side handshake.
helpviewer_keywords: ["WebSocketEndServerHandshake","WebSocketEndServerHandshake function [Websocket Protocol Component API]","websock.websocketendserverhandshake","websocket/WebSocketEndServerHandshake"]
old-location: websock\websocketendserverhandshake.htm
tech.root: WebSock
ms.assetid: 8708d290-18d6-4130-aa1c-8e4e5a716a5c
ms.date: 12/05/2018
ms.keywords: WebSocketEndServerHandshake, WebSocketEndServerHandshake function [Websocket Protocol Component API], websock.websocketendserverhandshake, websocket/WebSocketEndServerHandshake
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
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WebSocketEndServerHandshake
 - websocket/WebSocketEndServerHandshake
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - websocket.dll
api_name:
 - WebSocketEndServerHandshake
---

# WebSocketEndServerHandshake function


## -description

The <b>WebSocketEndServerHandshake</b> function completes the server-side handshake.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

## -returns

Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

## -remarks

This function may be called to complete the server-side handshake after a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginserverhandshake">WebSocketBeginServerHandshake</a>; however, calling this function is optional and applications may use the session functions without first calling this function. This function  frees all internal handshake related structures and allocates data session buffers. All operations handled by this function will be performed internally even if the function is not called.

## -see-also

<a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginclienthandshake">WebSocketBeginClientHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketbeginserverhandshake">WebSocketBeginServerHandshake</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketendclienthandshake">WebSocketEndClientHandshake</a>