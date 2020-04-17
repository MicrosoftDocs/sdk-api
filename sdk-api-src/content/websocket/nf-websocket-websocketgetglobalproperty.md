---
UID: NF:websocket.WebSocketGetGlobalProperty
title: WebSocketGetGlobalProperty function (websocket.h)
description: Gets a single WebSocket property.helpviewer_keywords: ["WebSocketGetGlobalProperty","WebSocketGetGlobalProperty function [Websocket Protocol Component API]","websock.websocketgetglobalproperty","websocket/WebSocketGetGlobalProperty"]
old-location: websock\websocketgetglobalproperty.htm
tech.root: WebSock
ms.assetid: ca4b76e9-6545-447b-93b2-e9e4054a54ec
ms.date: 12/05/2018
ms.keywords: WebSocketGetGlobalProperty, WebSocketGetGlobalProperty function [Websocket Protocol Component API], websock.websocketgetglobalproperty, websocket/WebSocketGetGlobalProperty
f1_keywords:
- websocket/WebSocketGetGlobalProperty
dev_langs:
- c++
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
- Websocket.dll
api_name:
- WebSocketGetGlobalProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WebSocketGetGlobalProperty function


## -description


The <b>WebSocketGetGlobalProperty</b> function  gets a single WebSocket property.


## -parameters




### -param eType [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/websocket/ns-websocket-web_socket_property">WEB_SOCKET_PROPERTY</a></b>

A WebSocket property.


### -param pvValue [in, out]

Type: <b>PVOID</b>

A pointer to the property value. The pointer must have an alignment compatible with the type of the property.


### -param ulSize [in, out]

Type: <b>ULONG*</b>

The size, in bytes, of the property pointed to by <b>pvValue</b>.


## -returns



Type: <b>HRESULT</b>

If the function succeeds, it returns <b>S_OK</b>.

If the function fails, it returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/websocket/ns-websocket-web_socket_property">WEB_SOCKET_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/websocket/ne-websocket-web_socket_property_type">WEB_SOCKET_PROPERTY_TYPE</a>
 

 

