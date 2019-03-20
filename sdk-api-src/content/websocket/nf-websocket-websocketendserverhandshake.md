---
UID: NF:websocket.WebSocketEndServerHandshake
title: WebSocketEndServerHandshake function (websocket.h)
author: windows-sdk-content
description: Completes the server-side handshake.
old-location: websock\websocketendserverhandshake.htm
tech.root: WebSock
ms.assetid: 8708d290-18d6-4130-aa1c-8e4e5a716a5c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WebSocketEndServerHandshake, WebSocketEndServerHandshake function [Websocket Protocol Component API], websock.websocketendserverhandshake, websocket/WebSocketEndServerHandshake
ms.topic: function
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
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - websocket.dll
api_name:
 - WebSocketEndServerHandshake
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WebSocketEndServerHandshake function


## -description


The <b>WebSocketEndServerHandshake</b> function completes the server-side handshake.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.




## -remarks



This function may be called to complete the server-side handshake after a previous call to <a href="https://msdn.microsoft.com/4009b56c-a92c-43fe-9e7b-2c38048aa748">WebSocketBeginServerHandshake</a>; however, calling this function is optional and applications may use the session functions without first calling this function. This function  frees all internal handshake related structures and allocates data session buffers. All operations handled by this function will be performed internally even if the function is not called.




## -see-also




<a href="https://msdn.microsoft.com/b326d32d-7226-46cd-b15b-b5547d3ec8cb">WebSocketBeginClientHandshake</a>



<a href="https://msdn.microsoft.com/4009b56c-a92c-43fe-9e7b-2c38048aa748">WebSocketBeginServerHandshake</a>



<a href="https://msdn.microsoft.com/07f2b2b8-1997-4ac7-b498-56d1e1fba9ef">WebSocketEndClientHandshake</a>
 

 

