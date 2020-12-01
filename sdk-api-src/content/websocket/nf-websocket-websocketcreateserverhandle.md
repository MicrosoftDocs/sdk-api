---
UID: NF:websocket.WebSocketCreateServerHandle
title: WebSocketCreateServerHandle function (websocket.h)
description: Creates a server-side WebSocket session handle.
helpviewer_keywords: ["WebSocketCreateServerHandle","WebSocketCreateServerHandle function [Websocket Protocol Component API]","websock.websocketcreateserverhandle","websocket/WebSocketCreateServerHandle"]
old-location: websock\websocketcreateserverhandle.htm
tech.root: WebSock
ms.assetid: f8c44a86-c586-48e3-b948-ed119bebf951
ms.date: 12/05/2018
ms.keywords: WebSocketCreateServerHandle, WebSocketCreateServerHandle function [Websocket Protocol Component API], websock.websocketcreateserverhandle, websocket/WebSocketCreateServerHandle
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
 - WebSocketCreateServerHandle
 - websocket/WebSocketCreateServerHandle
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
 - WebSocketCreateServerHandle
---

# WebSocketCreateServerHandle function


## -description

The <b>WebSocketCreateServerHandle</b> function creates a server-side WebSocket session handle.

## -parameters

### -param pProperties [in]

Type: <b>const <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_property">PWEB_SOCKET_PROPERTY</a></b>

Pointer to an array of <a href="/windows/desktop/api/websocket/ns-websocket-web_socket_property">WEB_SOCKET_PROPERTY</a> structures that contain WebSocket session-related properties.

### -param ulPropertyCount [in]

Type: <b>ULONG</b>

Number of properties in <i>pProperties</i>.

### -param phWebSocket [out]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a>*</b>

On successful output, pointer to a newly allocated server-side WebSocket session handle.

## -returns

Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/websocket/ns-websocket-web_socket_property">WEB_SOCKET_PROPERTY</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketaborthandle">WebSocketAbortHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketdeletehandle">WebSocketDeleteHandle</a>