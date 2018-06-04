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

# _tagSYNCMGRREGISTERFLAGS enumeration


## -description


The <b>SYNCMGRREGISTERFLAGS</b> enumeration values are used in methods of the <a href="https://msdn.microsoft.com/1feed230-5a50-4ff5-a8a9-e0ce15ba8f1c">ISyncMgrRegister</a> interface to identify events for which the handler is registered to be notified.


## -enum-fields




### -field SYNCMGRREGISTERFLAG_CONNECT

Network connect events.


### -field SYNCMGRREGISTERFLAG_PENDINGDISCONNECT

Pending network disconnect event.


### -field SYNCMGRREGISTERFLAG_IDLE

Idle events.


## -remarks



The SYNCMGRREGISTERFLAGS_MASK value can be used to identify valid <b>SYNCMGRREGISTERFLAGS</b> values.



