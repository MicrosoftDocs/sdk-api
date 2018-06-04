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
 

 

