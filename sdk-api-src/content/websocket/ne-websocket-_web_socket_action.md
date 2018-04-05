---
UID: NE:websocket._WEB_SOCKET_ACTION
title: "_WEB_SOCKET_ACTION"
author: windows-driver-content
description: Specifies actions to be taken by WebSocket applications.
old-location: websock\web_socket_action.htm
old-project: WebSock
ms.assetid: 46d22fb5-adc3-4d1c-81b8-480f1c6de327
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PWEB_SOCKET_ACTION, PWEB_SOCKET_ACTION, PWEB_SOCKET_ACTION enumeration pointer [Websocket Protocol Component API], WEB_SOCKET_ACTION, WEB_SOCKET_ACTION enumeration [Websocket Protocol Component API], WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION, WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION, WEB_SOCKET_NO_ACTION, WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION, WEB_SOCKET_SEND_TO_NETWORK_ACTION, _WEB_SOCKET_ACTION, websock.web_socket_action, websocket/PWEB_SOCKET_ACTION, websocket/WEB_SOCKET_ACTION, websocket/WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION, websocket/WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION, websocket/WEB_SOCKET_NO_ACTION, websocket/WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION, websocket/WEB_SOCKET_SEND_TO_NETWORK_ACTION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: WEB_SOCKET_ACTION, *PWEB_SOCKET_ACTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Websocket.h
api_name:
-	WEB_SOCKET_ACTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WEB_SOCKET_ACTION enumeration


## -description


The <b>WEB_SOCKET_ACTION</b> enumeration specifies actions to be taken by WebSocket  applications.


## -enum-fields




### -field WEB_SOCKET_NO_ACTION

There are no actions to process.


### -field WEB_SOCKET_SEND_TO_NETWORK_ACTION

Indicates the application should send the buffers to a network.


### -field WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION

Indicates the operation queued by <a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a> is complete. The application context returned by <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a> for this send operation is no longer needed, therefore it should be freed.


### -field WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION

Indicates the application should fill the buffers with data from a network.


### -field WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION

Indicates the operation queued by <a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a> is complete. The application context returned by <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a> for this receive operation is no longer needed, therefore it should be freed.


## -see-also




<a href="https://msdn.microsoft.com/59550c5a-a378-4162-a1cc-ed2d05662637">WEB_SOCKET_ACTION_QUEUE</a>



<a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>



<a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>



<a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>



<a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>
 

 

