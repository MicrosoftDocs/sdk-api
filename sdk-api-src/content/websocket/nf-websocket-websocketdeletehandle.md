---
UID: NF:websocket.WebSocketDeleteHandle
title: WebSocketDeleteHandle function (websocket.h)
description: Deletes a WebSocket session handle created by WebSocketCreateClientHandle or WebSocketCreateServerHandle.
helpviewer_keywords: ["WebSocketDeleteHandle","WebSocketDeleteHandle function [Websocket Protocol Component API]","websock.websocketdeletehandle","websocket/WebSocketDeleteHandle"]
old-location: websock\websocketdeletehandle.htm
tech.root: WebSock
ms.assetid: 0ee21ee8-1375-4b42-8d04-64368e299b3e
ms.date: 12/05/2018
ms.keywords: WebSocketDeleteHandle, WebSocketDeleteHandle function [Websocket Protocol Component API], websock.websocketdeletehandle, websocket/WebSocketDeleteHandle
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
 - WebSocketDeleteHandle
 - websocket/WebSocketDeleteHandle
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
 - WebSocketDeleteHandle
---

# WebSocketDeleteHandle function


## -description

The <b>WebSocketDeleteHandle</b> function deletes a WebSocket session handle created by <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

## -parameters

### -param hWebSocket [in]

Type: <b><a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a></b>

WebSocket session handle returned by a previous call to <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a> or <a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>.

## -returns

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

## -remarks

Any use of a deleted <a href="/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a> session handle may result in an access violation.

Before an application deletes a session handle, it must ensure that all operations have been processed. Applications may use <a href="/windows/desktop/api/websocket/nf-websocket-websocketaborthandle">WebSocketAbortHandle</a> to abort any queued operations before calling <b>WebSocketDeleteHandle</b>.

## -see-also

<a href="/windows/desktop/api/websocket/nf-websocket-websocketaborthandle">WebSocketAbortHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle">WebSocketCreateClientHandle</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>