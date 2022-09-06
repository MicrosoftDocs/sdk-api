---
UID: NE:websocket._WEB_SOCKET_ACTION_QUEUE
title: WEB_SOCKET_ACTION_QUEUE (websocket.h)
description: Specifies the action types returned by WebSocketGetAction.
helpviewer_keywords: ["WEB_SOCKET_ACTION_QUEUE","WEB_SOCKET_ACTION_QUEUE enumeration [Websocket Protocol Component API]","WEB_SOCKET_ALL_ACTION_QUEUE","WEB_SOCKET_RECEIVE_ACTION_QUEUE","WEB_SOCKET_SEND_ACTION_QUEUE","websock.web_socket_action_queue","websocket/WEB_SOCKET_ACTION_QUEUE","websocket/WEB_SOCKET_ALL_ACTION_QUEUE","websocket/WEB_SOCKET_RECEIVE_ACTION_QUEUE","websocket/WEB_SOCKET_SEND_ACTION_QUEUE"]
old-location: websock\web_socket_action_queue.htm
tech.root: WebSock
ms.assetid: 59550c5a-a378-4162-a1cc-ed2d05662637
ms.date: 12/05/2018
ms.keywords: WEB_SOCKET_ACTION_QUEUE, WEB_SOCKET_ACTION_QUEUE enumeration [Websocket Protocol Component API], WEB_SOCKET_ALL_ACTION_QUEUE, WEB_SOCKET_RECEIVE_ACTION_QUEUE, WEB_SOCKET_SEND_ACTION_QUEUE, websock.web_socket_action_queue, websocket/WEB_SOCKET_ACTION_QUEUE, websocket/WEB_SOCKET_ALL_ACTION_QUEUE, websocket/WEB_SOCKET_RECEIVE_ACTION_QUEUE, websocket/WEB_SOCKET_SEND_ACTION_QUEUE
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
req.typenames: WEB_SOCKET_ACTION_QUEUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WEB_SOCKET_ACTION_QUEUE
 - websocket/_WEB_SOCKET_ACTION_QUEUE
 - WEB_SOCKET_ACTION_QUEUE
 - websocket/WEB_SOCKET_ACTION_QUEUE
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
 - WEB_SOCKET_ACTION_QUEUE
---

# WEB_SOCKET_ACTION_QUEUE enumeration


## -description

The <b>WEB_SOCKET_ACTION_QUEUE</b> enumeration specifies the action types returned by <a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>.

## -enum-fields

### -field WEB_SOCKET_SEND_ACTION_QUEUE:0x1

<a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a> will return only send-related actions.

### -field WEB_SOCKET_RECEIVE_ACTION_QUEUE:0x2

<a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a> will return receive-related actions as well as internal send actions (reply to a ping frame).

### -field WEB_SOCKET_ALL_ACTION_QUEUE

<a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a> will return all actions.

## -see-also

<a href="/windows/desktop/api/websocket/ne-websocket-web_socket_action">WEB_SOCKET_ACTION</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>



<a href="/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>
