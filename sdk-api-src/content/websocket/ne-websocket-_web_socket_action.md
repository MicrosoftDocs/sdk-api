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

# _WEB_SOCKET_ACTION enumeration


## -description


The <b>WEB_SOCKET_ACTION</b> enumeration specifies actions to be taken by WebSocket  applications.


## -enum-fields




### -field WEB_SOCKET_NO_ACTION

There are no actions to process.


### -field WEB_SOCKET_SEND_TO_NETWORK_ACTION

Indicates the application should send the buffers to a network.


### -field WEB_SOCKET_INDICATE_SEND_COMPLETE_ACTION

Indicates the operation queued by <a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a> is complete. The application context returned by <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a> for this send operation is no longer needed, therefore it should be freed.


### -field WEB_SOCKET_RECEIVE_FROM_NETWORK_ACTION

Indicates the application should fill the buffers with data from a network.


### -field WEB_SOCKET_INDICATE_RECEIVE_COMPLETE_ACTION

Indicates the operation queued by <a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a> is complete. The application context returned by <a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a> for this receive operation is no longer needed, therefore it should be freed.


## -see-also




<a href="https://msdn.microsoft.com/59550c5a-a378-4162-a1cc-ed2d05662637">WEB_SOCKET_ACTION_QUEUE</a>



<a href="https://msdn.microsoft.com/e9b90176-c76f-42c2-b378-834a690bfe72">WebSocketCompleteAction</a>



<a href="https://msdn.microsoft.com/566cff2d-15dd-45c6-bc41-550be1f45cfd">WebSocketGetAction</a>



<a href="https://msdn.microsoft.com/6285c6fc-1f7a-45f3-ba28-94992e73693e">WebSocketReceive</a>



<a href="https://msdn.microsoft.com/289f3880-22ed-44f8-8a69-1c983153ea72">WebSocketSend</a>
 

 

