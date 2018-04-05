---
UID: NF:websocket.WebSocketGetGlobalProperty
title: WebSocketGetGlobalProperty function
author: windows-driver-content
description: Gets a single WebSocket property.
old-location: websock\websocketgetglobalproperty.htm
old-project: WebSock
ms.assetid: ca4b76e9-6545-447b-93b2-e9e4054a54ec
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WebSocketGetGlobalProperty, WebSocketGetGlobalProperty function [Websocket Protocol Component API], websock.websocketgetglobalproperty, websocket/WebSocketGetGlobalProperty
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WEB_SOCKET_PROPERTY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Websocket.dll
api_name:
-	WebSocketGetGlobalProperty
product: Windows
targetos: Windows
req.lib: Websocket.lib
req.dll: Websocket.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WebSocketGetGlobalProperty function


## -description


The <b>WebSocketGetGlobalProperty</b> function  gets a single WebSocket property.


## -parameters




### -param eType [in]

Type: <b><a href="https://msdn.microsoft.com/c8b35288-4cc1-4839-a5be-4fd13b162c20">WEB_SOCKET_PROPERTY</a></b>

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

If the function fails, it returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/c8b35288-4cc1-4839-a5be-4fd13b162c20">WEB_SOCKET_PROPERTY</a>



<a href="https://msdn.microsoft.com/d9442e90-a74f-452d-b1b5-9f4285b39f10">WEB_SOCKET_PROPERTY_TYPE</a>
 

 

