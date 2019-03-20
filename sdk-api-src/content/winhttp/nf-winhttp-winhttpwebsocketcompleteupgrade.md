---
UID: NF:winhttp.WinHttpWebSocketCompleteUpgrade
title: WinHttpWebSocketCompleteUpgrade function (winhttp.h)
author: windows-sdk-content
description: Completes a WebSocket handshake started by WinHttpSendRequest.
old-location: http\winhttpwebsocketcompleteupgrade.htm
tech.root: WinHttp
ms.assetid: a5d5971b-ac76-4be5-b884-a0e5ef9a495a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WinHttpWebSocketCompleteUpgrade, WinHttpWebSocketCompleteUpgrade function [WinHTTP], http.winhttpwebsocketcompleteupgrade, winhttp/WinHttpWebSocketCompleteUpgrade
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpWebSocketCompleteUpgrade
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinHttpWebSocketCompleteUpgrade function


## -description


The <b>WinHttpWebSocketCompleteUpgrade</b> function completes a WebSocket handshake started by <a href="https://msdn.microsoft.com/991bf531-2e6b-4581-8069-f75789915522">WinHttpSendRequest</a>.


## -parameters




### -param hRequest [in]

Type: <b>HINTERNET</b>

HTTP request handle used to send a WebSocket handshake.


### -param pContext [in, optional]

Type: <b>DWORD_PTR</b>

Context to be associated with the new handle.


## -returns



Type: <b>HINTERNET</b>

A new WebSocket handle. If NULL, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to determine the cause of failure.




## -remarks



<b>WinHttpWebSocketCompleteUpgrade</b> can be called on an open HTTP request to get a WebSocket handle for performing other WebSocket operations.

The request handle must be marked as a WebSocket upgrade by calling <a href="https://msdn.microsoft.com/bcf1da09-5787-4d2a-82ae-6965e27fa477">WinHttpSetOption</a> with <b>WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET</b> before sending the request.

The caller should check the HTTP status code returned by the server and call this function only if the status code was 101. Calling it with any other status code will result in a failure.



