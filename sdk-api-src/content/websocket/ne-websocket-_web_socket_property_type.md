---
UID: NE:websocket._WEB_SOCKET_PROPERTY_TYPE
title: "_WEB_SOCKET_PROPERTY_TYPE"
author: windows-sdk-content
description: Specifies a WebSocket property type.
old-location: websock\web_socket_property_type.htm
old-project: WebSock
ms.assetid: d9442e90-a74f-452d-b1b5-9f4285b39f10
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: WEB_SOCKET_ALLOCATED_BUFFER_PROPERTY_TYPE, WEB_SOCKET_DISABLE_MASKING_PROPERTY_TYPE, WEB_SOCKET_DISABLE_UTF8_VERIFICATION_PROPERTY_TYPE, WEB_SOCKET_KEEPALIVE_INTERVAL_PROPERTY_TYPE, WEB_SOCKET_PROPERTY_TYPE, WEB_SOCKET_PROPERTY_TYPE enumeration [Websocket Protocol Component API], WEB_SOCKET_RECEIVE_BUFFER_SIZE_PROPERTY_TYPE, WEB_SOCKET_SEND_BUFFER_SIZE_PROPERTY_TYPE, WEB_SOCKET_SUPPORTED_VERSIONS_PROPERTY_TYPE, _WEB_SOCKET_PROPERTY_TYPE, websock.web_socket_property_type, websocket/WEB_SOCKET_ALLOCATED_BUFFER_PROPERTY_TYPE, websocket/WEB_SOCKET_DISABLE_MASKING_PROPERTY_TYPE, websocket/WEB_SOCKET_DISABLE_UTF8_VERIFICATION_PROPERTY_TYPE, websocket/WEB_SOCKET_KEEPALIVE_INTERVAL_PROPERTY_TYPE, websocket/WEB_SOCKET_PROPERTY_TYPE, websocket/WEB_SOCKET_RECEIVE_BUFFER_SIZE_PROPERTY_TYPE, websocket/WEB_SOCKET_SEND_BUFFER_SIZE_PROPERTY_TYPE, websocket/WEB_SOCKET_SUPPORTED_VERSIONS_PROPERTY_TYPE
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Websocket.h
api_name:
-	WEB_SOCKET_PROPERTY_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WEB_SOCKET_PROPERTY_TYPE enumeration


## -description


The <b>WEB_SOCKET_PROPERTY_TYPE</b> enumeration specifies a WebSocket property type.


## -enum-fields




### -field WEB_SOCKET_RECEIVE_BUFFER_SIZE_PROPERTY_TYPE

Property type: <b>ULONG</b>

The WebSocket property is the internal receive buffer size. The buffer cannot be smaller than 256 bytes.

The default is 4096.

Used with <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> and <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>. 


### -field WEB_SOCKET_SEND_BUFFER_SIZE_PROPERTY_TYPE

Property type: <b>ULONG</b>

The WebSocket property is the internal send buffer size. The buffer cannot be smaller than 256 bytes.

The default is 4096 on a handle created with <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a>, and 16 on a handle created with <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.

Used with <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> and <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>. 


### -field WEB_SOCKET_DISABLE_MASKING_PROPERTY_TYPE

Property type:  <b>BOOL</b>

The WebSocket property is the disabling of the mask bit in client frames. On the client, this property sets the mask key to 0. On the server, this property  allows the server to accept client frames with the mask bit set to 0. This property may have serious security implications.
By default, this property is not used and masking is enabled.

Used with <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> and <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>. 


### -field WEB_SOCKET_ALLOCATED_BUFFER_PROPERTY_TYPE

Property type: <b>PVOID</b>

The WebSocket property is the buffer that is used as an internal buffer. If the passed buffer is not used, the WebSocket library will take care of buffer management.
The passed buffer must be aligned to an 8-byte boundary and be greater in size than the  receive buffer size + send buffer size + 256 bytes.

Used with <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> and <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>. 


### -field WEB_SOCKET_DISABLE_UTF8_VERIFICATION_PROPERTY_TYPE

Property type: <b>BOOL</b>

The WebSocket property disables UTF-8 verification.

Used with <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a> and <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>. 


### -field WEB_SOCKET_KEEPALIVE_INTERVAL_PROPERTY_TYPE

Property type: <b>ULONG</b>

The WebSocket property is the interval, in milliseconds, to send a keep-alive packet over the connection. The default interval is 30000 (30 seconds). The minimum interval is 15000 (15 seconds).
 <div class="alert"><b>Note</b>  The default value for the keep-alive interval is read from <b>HKLM:\SOFTWARE\Microsoft\WebSocket\KeepaliveInterval</b>. If a value is not set, the default value of 30000 will be used. It is not possible to have a lower keepalive interval than 15000 milliseconds. If a lower value is set, 15000 milliseconds will be used.</div>
<div> </div>


Used with <a href="https://msdn.microsoft.com/ca4b76e9-6545-447b-93b2-e9e4054a54ec">WebSocketGetGlobalProperty</a>. 


### -field WEB_SOCKET_SUPPORTED_VERSIONS_PROPERTY_TYPE

Property type: <b>ULONG</b> array

The WebSocket property is the versions of the WebSocket protocol that are supported.
 

Used with <a href="https://msdn.microsoft.com/ca4b76e9-6545-447b-93b2-e9e4054a54ec">WebSocketGetGlobalProperty</a>. 


## -see-also




<a href="https://msdn.microsoft.com/c8b35288-4cc1-4839-a5be-4fd13b162c20">WEB_SOCKET_PROPERTY</a>



<a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>



<a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>
 

 

