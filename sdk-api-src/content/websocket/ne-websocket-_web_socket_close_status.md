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
 

 

