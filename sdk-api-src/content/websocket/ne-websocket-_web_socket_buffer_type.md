---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WEB_SOCKET_BUFFER_TYPE enumeration


## -description


The <b>WEB_SOCKET_BUFFER_TYPE</b> enumeration specifies the bit values used to construct the WebSocket frame header.


## -enum-fields




### -field WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE

Indicates the buffer contains the last, and possibly only, part of a UTF8 message.


### -field WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE

Indicates the buffer contains part of a UTF8 message.


### -field WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE

Indicates the buffer contains the last, and possibly only, part of a binary message.


### -field WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE

Indicates the buffer contains part of a binary message.


### -field WEB_SOCKET_CLOSE_BUFFER_TYPE

Indicates the buffer contains a close message.


### -field WEB_SOCKET_PING_PONG_BUFFER_TYPE

Indicates the buffer contains a ping or pong message. When sending, this value means 'ping', when processing received data, this value means 'pong'.


### -field WEB_SOCKET_UNSOLICITED_PONG_BUFFER_TYPE

Indicates the buffer contains an unsolicited pong message.


## -remarks



Please note that the *FRAGMENT* and *MESSAGE* buffer types may not correspond to how the message appears (or is framed) on the wire. For example, when a single unfragmented 1000-byte message is received, WebSocket.dll may return multiple *FRAGMENT* buffer types followed by a single *MESSAGE* buffer type (with the sizes adding up to 1000).

Extension WebSocket frame headers (allowing reserved bits to be set by extensions) may be constructed by setting the high bit (MSB) and low bit (LSB) to 0. The remaining 9 lowest bits can then be used to form the custom frame header in place of the <b>WEB_SOCKET_BUFFER_TYPE</b> enumeration values.




## -see-also




<a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>



<a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>



<a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>
 

 

