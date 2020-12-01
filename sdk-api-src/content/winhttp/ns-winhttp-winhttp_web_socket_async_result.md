---
UID: NS:winhttp._WINHTTP_WEB_SOCKET_ASYNC_RESULT
title: WINHTTP_WEB_SOCKET_ASYNC_RESULT (winhttp.h)
description: The WINHTTP_WEB_SOCKET_ASYNC_RESULT includes the result status of a WebSocket operation.
helpviewer_keywords: ["WINHTTP_WEB_SOCKET_ASYNC_RESULT","WINHTTP_WEB_SOCKET_ASYNC_RESULT structure [HTTP]","http.http_web_socket_async_result","http.winhttp_web_socket_async_result","winhttp/WINHTTP_WEB_SOCKET_ASYNC_RESULT"]
old-location: http\winhttp_web_socket_async_result.htm
tech.root: http
ms.assetid: 90424980-9e30-465d-b948-820251c05357
ms.date: 12/05/2018
ms.keywords: WINHTTP_WEB_SOCKET_ASYNC_RESULT, WINHTTP_WEB_SOCKET_ASYNC_RESULT structure [HTTP], http.http_web_socket_async_result, http.winhttp_web_socket_async_result, winhttp/WINHTTP_WEB_SOCKET_ASYNC_RESULT
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
req.typenames: WINHTTP_WEB_SOCKET_ASYNC_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_WEB_SOCKET_ASYNC_RESULT
 - winhttp/_WINHTTP_WEB_SOCKET_ASYNC_RESULT
 - WINHTTP_WEB_SOCKET_ASYNC_RESULT
 - winhttp/WINHTTP_WEB_SOCKET_ASYNC_RESULT
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
 - WINHTTP_WEB_SOCKET_ASYNC_RESULT
---

# WINHTTP_WEB_SOCKET_ASYNC_RESULT structure


## -description

 The <b>WINHTTP_WEB_SOCKET_ASYNC_RESULT</b> includes the result status of a WebSocket operation.

## -struct-fields

### -field AsyncResult

Type: <b><a href="/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result">WINHTTP_ASYNC_RESULT</a></b>

The result of a WebSocket operation.

### -field Operation

Type: <b><a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_operation">WINHTTP_WEB_SOCKET_OPERATION</a></b>

The type of WebSocket operation.

## -remarks

A <b>WINHTTP_WEB_SOCKET_ASYNC_RESULT</b> structure is passed to the completion callbacks of WebSocket functions such as <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend">WinHttpWebSocketSend</a>, <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive">WinHttpWebSocketReceive</a>, and <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose">WinHttpWebSocketClose</a> when <i>dwInternetStatus</i> is <b>WINHTTP_CALLBACK_STATUS_REQUEST_ERROR</b>.

## -see-also

<a href="/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result">WINHTTP_ASYNC_RESULT</a>



<a href="/windows/desktop/api/winhttp/ne-winhttp-winhttp_web_socket_operation">WINHTTP_WEB_SOCKET_OPERATION</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose">WinHttpWebSocketClose</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive">WinHttpWebSocketReceive</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend">WinHttpWebSocketSend</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown">WinHttpWebSocketShutdown</a>