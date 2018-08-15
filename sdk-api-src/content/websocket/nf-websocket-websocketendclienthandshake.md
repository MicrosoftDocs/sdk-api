---
UID: NF:websocket.WebSocketEndClientHandshake
title: WebSocketEndClientHandshake function
author: windows-sdk-content
description: Completes the client-side handshake.
old-location: websock\websocketendclienthandshake.htm
old-project: WebSock
ms.assetid: 07f2b2b8-1997-4ac7-b498-56d1e1fba9ef
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WebSocketEndClientHandshake, WebSocketEndClientHandshake function [Websocket Protocol Component API], websock.websocketendclienthandshake, websocket/WebSocketEndClientHandshake
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
 - WebSocketEndClientHandshake
product: Windows
targetos: Windows
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WebSocketEndClientHandshake function


## -description


The <b>WebSocketEndClientHandshake</b> function completes the client-side handshake.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/c61992cc-7715-4fad-a66a-916402088ad0">WebSocketCreateClientHandle</a>.


### -param pResponseHeaders [in]

Type: <b>const <a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">PWEB_SOCKET_HTTP_HEADER</a></b>

Pointer to an array or <a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">WEB_SOCKET_HTTP_HEADER</a> structures that contain the response headers received by the application.


### -param ulReponseHeaderCount [in]

Type: <b>ULONG</b>

Number of response headers in <i>pResponseHeaders</i>.


### -param pulSelectedExtensions [in, out, optional]

Type: <b>ULONG*</b>

On input, pointer to an array allocated by the application. On successful output, pointer to an array of numbers that represent the extensions chosen by the server during the client-server handshake. These number are the zero-based indices into the extensions array passed to  <i>pszExtensions</i> in <a href="https://msdn.microsoft.com/b326d32d-7226-46cd-b15b-b5547d3ec8cb">WebSocketBeginClientHandshake</a>.


### -param pulSelectedExtensionCount [in, out, optional]

Type: <b>ULONG*</b>

On input, number of extensions allocated in <i>pulSelectedExtensions</i>. This must be at least equal to the number passed to <i>ulExtensionCount</i> in <b>WebSocketEndClientHandshake</b>. On successful output, number of extensions returned in <i>pulSelectedExtensions</i>.


### -param pulSelectedSubprotocol [in, out, optional]

Type: <b>ULONG*</b>

On successful output, pointer to a number that represents the sub-protocol chosen by the server during the client-server handshake. This number is the zero-based index into the sub-protocols array passed to  <i>pszSubprotocols</i> in <a href="https://msdn.microsoft.com/b326d32d-7226-46cd-b15b-b5547d3ec8cb">WebSocketBeginClientHandshake</a>.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns one of the following or a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALID_PROTOCOL_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Protocol data had an invalid format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNSUPPORTED_SUBPROTOCOL</b></dt>
</dl>
</td>
<td width="60%">
Server does not accept any of the sub-protocols specified by the application.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNSUPPORTED_EXTENSION</b></dt>
</dl>
</td>
<td width="60%">
Server does not accept extensions specified by the application.

</td>
</tr>
</table>
 




## -remarks



This function must be called to complete the client-side handshake after a previous call to <a href="https://msdn.microsoft.com/b326d32d-7226-46cd-b15b-b5547d3ec8cb">WebSocketBeginClientHandshake</a>. Once the client-server handshake is complete, the application may use the session functions.




## -see-also




<a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">WEB_SOCKET_HTTP_HEADER</a>



<a href="https://msdn.microsoft.com/b326d32d-7226-46cd-b15b-b5547d3ec8cb">WebSocketBeginClientHandshake</a>



<a href="https://msdn.microsoft.com/4009b56c-a92c-43fe-9e7b-2c38048aa748">WebSocketBeginServerHandshake</a>



<a href="https://msdn.microsoft.com/8708d290-18d6-4130-aa1c-8e4e5a716a5c">WebSocketEndServerHandshake</a>
 

 

