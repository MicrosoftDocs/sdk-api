---
UID: NF:winhttp.WinHttpWebSocketCompleteUpgrade
title: WinHttpWebSocketCompleteUpgrade function (winhttp.h)
description: Completes a WebSocket handshake started by WinHttpSendRequest.
helpviewer_keywords: ["WinHttpWebSocketCompleteUpgrade","WinHttpWebSocketCompleteUpgrade function [WinHTTP]","http.winhttpwebsocketcompleteupgrade","winhttp/WinHttpWebSocketCompleteUpgrade"]
old-location: http\winhttpwebsocketcompleteupgrade.htm
tech.root: http
ms.assetid: a5d5971b-ac76-4be5-b884-a0e5ef9a495a
ms.date: 12/05/2018
ms.keywords: WinHttpWebSocketCompleteUpgrade, WinHttpWebSocketCompleteUpgrade function [WinHTTP], http.winhttpwebsocketcompleteupgrade, winhttp/WinHttpWebSocketCompleteUpgrade
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
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinHttpWebSocketCompleteUpgrade
 - winhttp/WinHttpWebSocketCompleteUpgrade
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpWebSocketCompleteUpgrade
---

# WinHttpWebSocketCompleteUpgrade function


## -description

The <b>WinHttpWebSocketCompleteUpgrade</b> function completes a WebSocket handshake started by <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a>.

## -parameters

### -param hRequest [in]

Type: <b>HINTERNET</b>

HTTP request handle used to send a WebSocket handshake.

### -param pContext [in, optional]

Type: <b>DWORD_PTR</b>

Context to be associated with the new handle.

## -returns

Type: <b>HINTERNET</b>

A new WebSocket handle. If NULL, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to determine the cause of failure.

## -remarks

<b>WinHttpWebSocketCompleteUpgrade</b> can be called on an open HTTP request to get a WebSocket handle for performing other WebSocket operations.

The request handle must be marked as a WebSocket upgrade by calling <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsetoption">WinHttpSetOption</a> with <b>WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET</b> before sending the request.

The caller should check the HTTP status code returned by the server and call this function only if the status code was 101. Calling it with any other status code will result in a failure.