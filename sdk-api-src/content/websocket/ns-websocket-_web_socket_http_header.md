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

# _WEB_SOCKET_HTTP_HEADER structure


## -description


The <b>WEB_SOCKET_HTTP_HEADER</b> structure contains an HTTP header.


## -struct-fields




### -field pcName

Type: <b>PCHAR</b>

A pointer to the HTTP header name. The name must not  contain a colon character.


### -field ulNameLength

Type: <b>ULONG</b>

Length, in characters,  of the HTTP header pointed to by <b>pcName</b>.


### -field pcValue

Type: <b>PCHAR</b>

A pointer to the HTTP header value.


### -field ulValueLength

Type: <b>ULONG</b>

Length, in characters,  of the HTTP value pointed to by <b>pcValue</b>.


## -see-also




<a href="https://msdn.microsoft.com/b326d32d-7226-46cd-b15b-b5547d3ec8cb">WebSocketBeginClientHandshake</a>



<a href="https://msdn.microsoft.com/4009b56c-a92c-43fe-9e7b-2c38048aa748">WebSocketBeginServerHandshake</a>



<a href="https://msdn.microsoft.com/07f2b2b8-1997-4ac7-b498-56d1e1fba9ef">WebSocketEndClientHandshake</a>



<a href="https://msdn.microsoft.com/8708d290-18d6-4130-aa1c-8e4e5a716a5c">WebSocketEndServerHandshake</a>
 

 

