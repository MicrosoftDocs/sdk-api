---
UID: NF:websocket.WebSocketBeginClientHandshake
title: WebSocketBeginClientHandshake function
author: windows-sdk-content
description: Begins the client-side handshake.
old-location: websock\websocketbeginclienthandshake.htm
old-project: WebSock
ms.assetid: b326d32d-7226-46cd-b15b-b5547d3ec8cb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WebSocketBeginClientHandshake, WebSocketBeginClientHandshake function [Websocket Protocol Component API], websock.websocketbeginclienthandshake, websocket/WebSocketBeginClientHandshake
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: websocket.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - websocket.dll
api_name:
 - WebSocketBeginClientHandshake
product: Windows
targetos: Windows
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WebSocketBeginClientHandshake function


## -description


The <b>WebSocketBeginClientHandshake</b> function  begins the client-side handshake.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a>.


### -param pszSubprotocols [in, optional]

Type: <b>PCSTR*</b>

Pointer to an array of sub-protocols chosen by the application. Once the client-server handshake is complete, the application must use the sub-protocol returned by <a href="https://msdn.microsoft.com/07f2b2b8-1997-4ac7-b498-56d1e1fba9ef">WebSocketEndClientHandshake</a>. Must contain one subprotocol per entry.


### -param ulSubprotocolCount [in]

Type: <b>ULONG</b>

Number of sub-protocols in <i>pszSubprotocols</i>.


### -param pszExtensions [in, optional]

Type: <b>PCSTR*</b>

Pointer to an array of extensions chosen by the application. Once the client-server handshake is complete, the application must use the extension returned by <a href="https://msdn.microsoft.com/07f2b2b8-1997-4ac7-b498-56d1e1fba9ef">WebSocketEndClientHandshake</a>. Must contain one extension per entry.


### -param ulExtensionCount [in]

Type: <b>ULONG</b>

Number of extensions in <i>pszExtensions</i>.


### -param pInitialHeaders [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">PWEB_SOCKET_HTTP_HEADER</a></b>

Pointer to an array of <a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">WEB_SOCKET_HTTP_HEADER</a> structures that contain the request headers to be sent by the application. The array must include the <i>Host HTTP</i> header as defined in <a href="http://go.microsoft.com/fwlink/p/?LinkID=241642">RFC 2616</a>.


### -param ulInitialHeaderCount [in]

Type: <b>ULONG</b>

Number of request headers in <i>pInitialHeaders</i>.


### -param pAdditionalHeaders [out]

Type: <b><a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">PWEB_SOCKET_HTTP_HEADER</a></b>

On successful output, pointer to an array of <a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">WEB_SOCKET_HTTP_HEADER</a> structures that contain the request headers to be sent by the application. If any of these headers were specified in <i>pInitialHeaders</i>, the header must be replaced.


### -param pulAdditionalHeaderCount [out]

Type: <b>ULONG*</b>

On successful output, number of response headers in <i>pAdditionalHeaders</i>.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.




## -remarks



To complete the client-side handshake, applications must call <a href="https://msdn.microsoft.com/07f2b2b8-1997-4ac7-b498-56d1e1fba9ef">WebSocketEndClientHandshake</a>. Once the client-server handshake is complete, the application may use the session functions.




## -see-also




<a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">WEB_SOCKET_HTTP_HEADER</a>



<a href="https://msdn.microsoft.com/4009b56c-a92c-43fe-9e7b-2c38048aa748">WebSocketBeginServerHandshake</a>



<a href="https://msdn.microsoft.com/07f2b2b8-1997-4ac7-b498-56d1e1fba9ef">WebSocketEndClientHandshake</a>



<a href="https://msdn.microsoft.com/8708d290-18d6-4130-aa1c-8e4e5a716a5c">WebSocketEndServerHandshake</a>
 

 

