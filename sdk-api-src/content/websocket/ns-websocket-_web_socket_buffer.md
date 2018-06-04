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

# _WEB_SOCKET_BUFFER structure


## -description


The <b>WEB_SOCKET_BUFFER</b> structure contains data for a specific WebSocket action.


## -struct-fields




### -field Data


### -field Data.pbBuffer

<b>Type: <b>PBYTE</b>
</b>
Pointer to the WebSocket buffer data.


### -field Data.ulBufferLength

<b>Type: <b>ULONG</b>
</b>
Length, in bytes, of the buffer pointed to by <b>pbBuffer</b>.


### -field CloseStatus


### -field CloseStatus.pbReason

<b>Type: <b>PBYTE</b>
</b>
A point to a UTF-8 string that represents the reason the connection is closed. If <b>ulReasonLength</b> is 0, this must be <b>NULL</b>.


### -field CloseStatus.ulReasonLength

<b>Type: <b>ULONG</b>
</b>
Length, in bytes, of the buffer pointed to by <b>pbReason</b>. It cannot exceed <b>WEB_SOCKET_MAX_CLOSE_REASON_LENGTH</b> (123 bytes).


### -field CloseStatus.usStatus

<b>Type: <b>USHORT</b>
</b>

<a href="https://msdn.microsoft.com/bd2c279c-ae6c-469a-8a97-d46fca042126">WEB_SOCKET_CLOSE_STATUS</a> enumeration that specifies the WebSocket status.


## -remarks



Application must use the <b>Data</b> struct for all buffer types except <b>WEB_SOCKET_CLOSE_BUFFER_TYPE</b>. The <b>CloseStatus</b> struct is used for <b>WEB_SOCKET_CLOSE_BUFFER_TYPE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a6657b51-ac16-4637-8dfd-e3dade951385">WEB_SOCKET_BUFFER_TYPE</a>



<a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>



<a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>



<a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>
 

 

