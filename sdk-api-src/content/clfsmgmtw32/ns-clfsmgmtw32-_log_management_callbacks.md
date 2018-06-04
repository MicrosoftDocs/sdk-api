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

# _LOG_MANAGEMENT_CALLBACKS structure


## -description


The <b>LOG_MANAGEMENT_CALLBACKS</b> structure is used to register with the Common Log File System (CLFS) for the callbacks that a client program requires information from.


## -struct-fields




### -field CallbackContext

A pointer to the context which is a client-defined value.  CLFS ignores this value other than to pass it with every callback to the client.


### -field AdvanceTailCallback

 Called when the management functionality determines that the client should advance the tail of its log.


### -field LogFullHandlerCallback

Called when an asynchronous request is initiated when <a href="https://msdn.microsoft.com/ed4b067f-9386-4bec-a6dc-b22d6fd52390">HandleLogFull</a> completes.


### -field LogUnpinnedCallback

Called when a pinned log becomes unpinned.

