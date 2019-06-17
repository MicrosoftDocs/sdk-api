---
UID: NF:websocket.WebSocketCreateClientHandle
title: WebSocketCreateClientHandle function (websocket.h)
author: windows-sdk-content
description: Creates a client-side WebSocket session handle.
old-location: websock\websocketcreateclienthandle.htm
tech.root: WebSock
ms.assetid: c61992cc-7715-4fad-a66a-916402088ad0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WebSocketCreateClientHandle, WebSocketCreateClientHandle function [Websocket Protocol Component API], websock.websocketcreateclienthandle, websocket/WebSocketCreateClientHandle
ms.topic: function
f1_keywords: ["websocket/WebSocketCreateClientHandle"]
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
 - WebSocketCreateClientHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WebSocketCreateClientHandle function


## -description


The <b>WebSocketCreateClientHandle</b> function creates a client-side WebSocket session handle.


## -parameters




### -param pProperties [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/websocket/ns-websocket-_web_socket_property">PWEB_SOCKET_PROPERTY</a></b>

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/websocket/ns-websocket-_web_socket_property">WEB_SOCKET_PROPERTY</a> structures that contain WebSocket session-related properties.


### -param ulPropertyCount [in]

Type: <b>ULONG</b>

Number of properties in <i>pProperties</i>.


### -param phWebSocket [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WebSock/web-socket-protocol-component-api-data-types">WEB_SOCKET_HANDLE</a>*</b>

On successful output, pointer to a  newly allocated client-side WebSocket session handle.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/websocket/ns-websocket-_web_socket_property">WEB_SOCKET_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketaborthandle">WebSocketAbortHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle">WebSocketCreateServerHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/websocket/nf-websocket-websocketdeletehandle">WebSocketDeleteHandle</a>
 

 

