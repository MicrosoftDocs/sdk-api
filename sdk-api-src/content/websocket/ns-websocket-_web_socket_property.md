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
 

 

