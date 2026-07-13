---
UID: NS:winhttp._WINHTTP_WEB_SOCKET_STATUS
title: WINHTTP_WEB_SOCKET_STATUS (winhttp.h)
description: The WINHTTP_WEB_SOCKET_STATUS enumeration includes the status of a WebSocket operation.
helpviewer_keywords: ["WINHTTP_WEB_SOCKET_STATUS","WINHTTP_WEB_SOCKET_STATUS structure [HTTP]","http.winhttp_web_socket_status","winhttp/WINHTTP_WEB_SOCKET_STATUS"]
old-location: http\winhttp_web_socket_status.htm
tech.root: http
ms.assetid: 4e34a306-1238-4a3b-8336-475e904b0a60
ms.date: 12/05/2018
ms.keywords: WINHTTP_WEB_SOCKET_STATUS, WINHTTP_WEB_SOCKET_STATUS structure [HTTP], http.winhttp_web_socket_status, winhttp/WINHTTP_WEB_SOCKET_STATUS
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
req.typenames: WINHTTP_WEB_SOCKET_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_WEB_SOCKET_STATUS
 - winhttp/_WINHTTP_WEB_SOCKET_STATUS
 - WINHTTP_WEB_SOCKET_STATUS
 - winhttp/WINHTTP_WEB_SOCKET_STATUS
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
 - WINHTTP_WEB_SOCKET_STATUS
---

# WINHTTP_WEB_SOCKET_STATUS structure


## -description

The <b>WINHTTP_WEB_SOCKET_STATUS</b> enumeration includes the status of a WebSocket operation.

## -struct-fields

### -field dwBytesTransferred

Type: <b>DWORD</b>

The amount of bytes transferred in the operation.

### -field eBufferType

Type: <b><a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_buffer_type">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a></b>

The type of data in the buffer.

## -remarks

A <b>WINHTTP_WEB_SOCKET_STATUS</b> structure is passed to the completion callback of <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend">WinHttpWebSocketSend</a> when <i>dwInternetStatus</i>  is <b>WINHTTP_CALLBACK_STATUS_READ_COMPLETE</b>.

A <b>WINHTTP_WEB_SOCKET_STATUS</b> structure is passed to the completion callback of <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive">WinHttpWebSocketReceive</a> when <i>dwInternetStatus</i>  is <b>WINHTTP_CALLBACK_STATUS_WRITE_COMPLETE</b>.

## -see-also

<a href="/windows/desktop/api/winhttp/nc-winhttp-winhttp_status_callback">WINHTTP_STATUS_CALLBACK</a>



<a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_buffer_type">WINHTTP_WEB_SOCKET_BUFFER_TYPE</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose">WinHttpWebSocketClose</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive">WinHttpWebSocketReceive</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend">WinHttpWebSocketSend</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown">WinHttpWebSocketShutdown</a>