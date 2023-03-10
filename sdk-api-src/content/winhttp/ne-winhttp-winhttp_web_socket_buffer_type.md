---
UID: NE:winhttp._WINHTTP_WEB_SOCKET_BUFFER_TYPE
title: WINHTTP_WEB_SOCKET_BUFFER_TYPE (winhttp.h)
description: The WINHTTP_WEB_SOCKET_BUFFER_TYPE enumeration includes types of WebSocket buffers.
helpviewer_keywords: ["WINHTTP_WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE","WINHTTP_WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE","WINHTTP_WEB_SOCKET_BUFFER_TYPE","WINHTTP_WEB_SOCKET_BUFFER_TYPE enumeration [HTTP]","WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE","WINHTTP_WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE","WINHTTP_WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE","http.winhttp_web_socket_buffer_type","winhttp/WINHTTP_WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE","winhttp/WINHTTP_WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE","winhttp/WINHTTP_WEB_SOCKET_BUFFER_TYPE","winhttp/WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE","winhttp/WINHTTP_WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE","winhttp/WINHTTP_WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE"]
old-location: http\winhttp_web_socket_buffer_type.htm
tech.root: http
ms.assetid: 9d730a6e-d05f-48ad-beec-cba6cc5cb17c
ms.date: 12/05/2018
ms.keywords: WINHTTP_WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE, WINHTTP_WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE, WINHTTP_WEB_SOCKET_BUFFER_TYPE, WINHTTP_WEB_SOCKET_BUFFER_TYPE enumeration [HTTP], WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE, WINHTTP_WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE, WINHTTP_WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE, http.winhttp_web_socket_buffer_type, winhttp/WINHTTP_WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE, winhttp/WINHTTP_WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE
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
targetos: Windows
req.typenames: WINHTTP_WEB_SOCKET_BUFFER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_WEB_SOCKET_BUFFER_TYPE
 - winhttp/_WINHTTP_WEB_SOCKET_BUFFER_TYPE
 - WINHTTP_WEB_SOCKET_BUFFER_TYPE
 - winhttp/WINHTTP_WEB_SOCKET_BUFFER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - WINHTTP_WEB_SOCKET_BUFFER_TYPE
---

# WINHTTP_WEB_SOCKET_BUFFER_TYPE enumeration


## -description

The <b>WINHTTP_WEB_SOCKET_BUFFER_TYPE</b> enumeration includes types of WebSocket buffers.

## -enum-fields

### -field WINHTTP_WEB_SOCKET_BINARY_MESSAGE_BUFFER_TYPE:0

Buffer contains either the entire binary message or the last part of it.

### -field WINHTTP_WEB_SOCKET_BINARY_FRAGMENT_BUFFER_TYPE:1

Buffer contains only part of a binary message.

### -field WINHTTP_WEB_SOCKET_UTF8_MESSAGE_BUFFER_TYPE:2

Buffer contains either the entire UTF-8 message or the last part of it.

### -field WINHTTP_WEB_SOCKET_UTF8_FRAGMENT_BUFFER_TYPE:3

Buffer contains only part of a UTF-8 message.

### -field WINHTTP_WEB_SOCKET_CLOSE_BUFFER_TYPE:4

The server sent a close frame.

