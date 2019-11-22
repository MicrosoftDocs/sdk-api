---
UID: NE:websocket._WEB_SOCKET_ACTION
title: WEB_SOCKET_ACTION (websocket.h)

description: Specifies actions to be taken by WebSocket applications.
old-location: websock\web_socket_action.htm
tech.root: WebSock
ms.assetid: 46d22fb5-adc3-4d1c-81b8-480f1c6de327

ms.date: 12/05/2018
ms.keywords: '*PWEB_SOCKET_ACTION, PWEB_SOCKET_ACTION, PWEB_SOCKET_ACTION enumeration pointer [Websocket Protocol Component API], WEB_SOCKET_ACTION, WEB_SOCKET_ACTION enumeration [Websocket Protocol Component API], WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION, WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION, WEB_SOCKET_NO_ACTION, WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION, WEB_SOCKET_SEND_TO_NETWORK_ACTION, websock.web_socket_action, websocket/PWEB_SOCKET_ACTION, websocket/WEB_SOCKET_ACTION, websocket/WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION, websocket/WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION, websocket/WEB_SOCKET_NO_ACTION, websocket/WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION, websocket/WEB_SOCKET_SEND_TO_NETWORK_ACTION'
ms.topic: enum
f1_keywords:
- websocket/WEB_SOCKET_ACTION
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Websocket.h
api_name:
- WEB_SOCKET_ACTION
targetos: Windows
req.typenames: WEB_SOCKET_ACTION, *PWEB_SOCKET_ACTION
req.redist: 
ms.custom: 19H1
---

# WEB_SOCKET_ACTION enumeration


## -description


The <b>WEB_SOCKET_ACTION</b> enumeration specifies actions to be taken by WebSocket  applications.


## -enum-fields




### -field WEB_SOCKET_NO_ACTION

There are no actions to process.


### -field WEB_SOCKET_SEND_TO_NETWORK_ACTION

Indicates the application should send the buffers to a network.


### -field WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION

Indicates the operation queued by <a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a> is complete. The application context returned by <a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a> for this send operation is no longer needed, therefore it should be freed.


### -field WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION

Indicates the application should fill the buffers with data from a network.


### -field WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION

Indicates the operation queued by <a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a> is complete. The application context returned by <a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a> for this receive operation is no longer needed, therefore it should be freed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/websocket/ne-websocket-web_socket_action_queue">WEB_SOCKET_ACTION_QUEUE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction">WebSocketCompleteAction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketgetaction">WebSocketGetAction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketreceive">WebSocketReceive</a>



<a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketsend">WebSocketSend</a>
 

 

