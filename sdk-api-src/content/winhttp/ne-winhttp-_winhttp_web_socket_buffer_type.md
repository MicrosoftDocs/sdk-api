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

# _WINHTTP_WEB_SOCKET_BUFFER_TYPE enumeration


## -description


The <b>WINHTTP_WEB_SOCKET_BUFFER_TYPE</b> enumeration includes types of WebSocket buffers.


## -enum-fields




### -field WINHTTP_WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE

Buffer contains either the entire binary message or the last part of it.


### -field WINHTTP_WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE

Buffer contains only part of a binary message.


### -field WINHTTP_WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE

Buffer contains either the entire UTF-8 message or the last part of it.


### -field WINHTTP_WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE

Buffer contains only part of a UTF-8 message.


### -field WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE

The server sent a close frame.

