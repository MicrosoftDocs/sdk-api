---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WebSocketBeginServerHandshake function


## -description


The <b>WebSocketBeginServerHandshake</b> function  begins the server-side handshake.


## -parameters




### -param hWebSocket [in]

Type: <b><a href="https://msdn.microsoft.com/D5D42785-CFAC-4324-9194-1BA8056FBAA1">WEB_SOCKET_HANDLE</a></b>

 WebSocket session handle returned by a previous call to <a href="https://msdn.microsoft.com/f8c44a86-c586-48e3-b948-ed119bebf951">WebSocketCreateServerHandle</a>.


### -param pszSubprotocolSelected [in, optional]

Type: <b>PCSTR</b>

A pointer to a sub-protocol value chosen by the application. Must contain one subprotocol.


### -param pszExtensionSelected [in, optional]

Type: <b>PCSTR*</b>

A pointer to a list of extensions chosen by the application. Must contain one extension per entry.


### -param ulExtensionSelectedCount [in]

Type: <b>ULONG</b>

Number of extensions in <i>pszExtensionSelected</i>.


### -param pRequestHeaders [in]

Type: <b>const <a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">PWEB_SOCKET_HTTP_HEADER</a></b>

Pointer to an array of <a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">WEB_SOCKET_HTTP_HEADER</a> structures that contain the request headers received by the application.


### -param ulRequestHeaderCount [in]

Type: <b>ULONG</b>

Number of request headers in <i>pRequestHeaders</i>.


### -param pResponseHeaders [out]

Type: <b><a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">PWEB_SOCKET_HTTP_HEADER</a>*</b>

On successful output, a pointer to an array or <a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">WEB_SOCKET_HTTP_HEADER</a> structures that contain the response headers to be sent by the application.


### -param pulResponseHeaderCount [out]

Type: <b>ULONG*</b>

On successful output, number of response headers in <i>pResponseHeaders</i>.


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
</table>
 




## -remarks



To complete the server-side handshake, applications must call <a href="https://msdn.microsoft.com/8708d290-18d6-4130-aa1c-8e4e5a716a5c">WebSocketEndServerHandshake</a> or any of the session functions. Once the client-server handshake is complete, the application may use the session functions.




## -see-also




<a href="https://msdn.microsoft.com/d051c2fd-c21c-43dc-9160-5626fb1d6d49">WEB_SOCKET_HTTP_HEADER</a>



<a href="https://msdn.microsoft.com/b326d32d-7226-46cd-b15b-b5547d3ec8cb">WebSocketBeginClientHandshake</a>



<a href="https://msdn.microsoft.com/07f2b2b8-1997-4ac7-b498-56d1e1fba9ef">WebSocketEndClientHandshake</a>



<a href="https://msdn.microsoft.com/8708d290-18d6-4130-aa1c-8e4e5a716a5c">WebSocketEndServerHandshake</a>
 

 

