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



