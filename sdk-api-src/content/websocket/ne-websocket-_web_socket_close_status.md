---
UID: NE:websocket._WEB_SOCKET_CLOSE_STATUS
title: "_WEB_SOCKET_CLOSE_STATUS"
author: windows-sdk-content
description: Specifies the WebSocket close status.
old-location: websock\web_socket_close_status.htm
old-project: WebSock
ms.assetid: bd2c279c-ae6c-469a-8a97-d46fca042126
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WEB_SOCKET_ABORTED_CLOSE_STATUS, WEB_SOCKET_CLOSE_STATUS, WEB_SOCKET_CLOSE_STATUS enumeration [Websocket Protocol Component API], WEB_SOCKET_EMPTY_CLOSE_STATUS, WEB_SOCKET_ENDPOINT_UNAVAILABLE_CLOSE_STATUS, WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS, WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS, WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS, WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS, WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS, WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS, WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS, WEB_SOCKET_SUCCESS_CLOSE_STATUS, WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS, _WEB_SOCKET_CLOSE_STATUS, websock.web_socket_close_status, websocket/WEB_SOCKET_ABORTED_CLOSE_STATUS, websocket/WEB_SOCKET_CLOSE_STATUS, websocket/WEB_SOCKET_EMPTY_CLOSE_STATUS, websocket/WEB_SOCKET_ENDPOINT_UNAVAILABLE_CLOSE_STATUS, websocket/WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS, websocket/WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS, websocket/WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS, websocket/WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS, websocket/WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS, websocket/WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS, websocket/WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS, websocket/WEB_SOCKET_SUCCESS_CLOSE_STATUS, websocket/WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: WEB_SOCKET_CLOSE_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Websocket.h
api_name:
 - WEB_SOCKET_CLOSE_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WEB_SOCKET_CLOSE_STATUS enumeration


## -description


The <b>WEB_SOCKET_CLOSE_STATUS</b> enumeration specifies the WebSocket close status as defined by <a href="http://go.microsoft.com/fwlink/p/?linkid=240293">WSPROTO</a>.


## -enum-fields




### -field WEB_SOCKET_SUCCESS_CLOSE_STATUS

Close completed successfully.


### -field WEB_SOCKET_ENDPOINT_UNAVAILABLE_CLOSE_STATUS

The endpoint is going away and thus closing the connection.


### -field WEB_SOCKET_PROTOCOL_ERROR_CLOSE_STATUS

Peer detected protocol error and it is closing the connection.


### -field WEB_SOCKET_INVALID_DATA_TYPE_CLOSE_STATUS

The endpoint cannot receive this type of data.


### -field WEB_SOCKET_EMPTY_CLOSE_STATUS

No close status
      code was provided.


### -field WEB_SOCKET_ABORTED_CLOSE_STATUS

The
      connection was closed without sending or
      receiving a close frame.



### -field WEB_SOCKET_INVALID_PAYLOAD_CLOSE_STATUS

Data within a message is not consistent with the type of the message.


### -field WEB_SOCKET_POLICY_VIOLATION_CLOSE_STATUS

The message violates an endpoint's policy.


### -field WEB_SOCKET_MESSAGE_TOO_BIG_CLOSE_STATUS

The message sent was too large to process.


### -field WEB_SOCKET_UNSUPPORTED_EXTENSIONS_CLOSE_STATUS

A client endpoint expected the server to negotiate one or more extensions, but the server didn't return them in the response message of the WebSocket handshake. 


### -field WEB_SOCKET_SERVER_ERROR_CLOSE_STATUS

An unexpected condition prevented the server from
      fulfilling the request.



### -field WEB_SOCKET_SECURE_HANDSHAKE_ERROR_CLOSE_STATUS

The
      TLS handshake could not be completed.


## -see-also




<a href="https://msdn.microsoft.com/05EC3940-4A17-4FBB-9446-15B511E18FF2">WEB_SOCKET_BUFFER</a>
 

 

