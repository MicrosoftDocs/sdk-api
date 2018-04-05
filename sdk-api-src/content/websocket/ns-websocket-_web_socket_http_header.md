---
UID: NS:websocket._WEB_SOCKET_HTTP_HEADER
title: "_WEB_SOCKET_HTTP_HEADER"
author: windows-driver-content
description: Contains an HTTP header.
old-location: websock\web_socket_http_header.htm
old-project: WebSock
ms.assetid: d051c2fd-c21c-43dc-9160-5626fb1d6d49
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PWEB_SOCKET_HTTP_HEADER, PWEB_SOCKET_HTTP_HEADER, PWEB_SOCKET_HTTP_HEADER structure pointer [Websocket Protocol Component API], WEB_SOCKET_HTTP_HEADER, WEB_SOCKET_HTTP_HEADER structure [Websocket Protocol Component API], _WEB_SOCKET_HTTP_HEADER, websock.web_socket_http_header, websocket/PWEB_SOCKET_HTTP_HEADER, websocket/WEB_SOCKET_HTTP_HEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WEB_SOCKET_HTTP_HEADER, *PWEB_SOCKET_HTTP_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Websocket.h
api_name:
-	WEB_SOCKET_HTTP_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

