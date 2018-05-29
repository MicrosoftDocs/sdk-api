---
UID: NS:websocket._WEB_SOCKET_PROPERTY
title: "_WEB_SOCKET_PROPERTY"
author: windows-sdk-content
description: Contains a single WebSocket property.
old-location: websock\web_socket_property.htm
old-project: WebSock
ms.assetid: c8b35288-4cc1-4839-a5be-4fd13b162c20
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PWEB_SOCKET_PROPERTY, PWEB_SOCKET_PROPERTY, PWEB_SOCKET_PROPERTY structure pointer [Websocket Protocol Component API], WEB_SOCKET_PROPERTY, WEB_SOCKET_PROPERTY structure [Websocket Protocol Component API], _WEB_SOCKET_PROPERTY, websock.web_socket_property, websocket/PWEB_SOCKET_PROPERTY, websocket/WEB_SOCKET_PROPERTY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Websocket.h
api_name:
-	WEB_SOCKET_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WEB_SOCKET_PROPERTY structure


## -description


The <b>WEB_SOCKET_PROPERTY</b> structure contains a  single WebSocket property.


## -struct-fields




### -field Type

Type: <b><a href="https://msdn.microsoft.com/d9442e90-a74f-452d-b1b5-9f4285b39f10">WEB_SOCKET_PROPERTY_TYPE</a></b>

The WebSocket property type.


### -field pvValue

Type: <b>PVOID</b>

A pointer to the value to set. The pointer must have an alignment compatible with the type of the property.


### -field ulValueSize

Type: <b>ULONG</b>

The size, in bytes, of the property pointed to by <b>pvValue</b>.


## -see-also




<a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a>



<a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>



<a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>



<a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>
 

 

