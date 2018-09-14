---
UID: NE:winhttp._WINHTTP_WEB_SOCKET_BUFFER_TYPE
title: "_WINHTTP_WEB_SOCKET_BUFFER_TYPE"
author: windows-sdk-content
description: The WINHTTP_WEB_SOCKET_BUFFER_TYPE enumeration includes types of WebSocket buffers.
old-location: http\winhttp_web_socket_buffer_type.htm
tech.root: winhttp
ms.assetid: 9d730a6e-d05f-48ad-beec-cba6cc5cb17c
ms.author: windowssdkdev
ms.date: 09/11/2018
ms.keywords: WINHTTP_WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE, WINHTTP_WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE, WINHTTP_WEB_SOCKET_BUFFER_TYPE, WINHTTP_WEB_SOCKET_BUFFER_TYPE enumeration [HTTP], WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE, WINHTTP_WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE, WINHTTP_WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE, _WINHTTP_WEB_SOCKET_BUFFER_TYPE, http.winhttp_web_socket_buffer_type, winhttp/WINHTTP_WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winhttp.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - WINHTTP_WEB_SOCKET_BUFFER_TYPE
product: Windows
targetos: Windows
req.typenames: WINHTTP_WEB_SOCKET_BUFFER_TYPE
req.redist: 
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

