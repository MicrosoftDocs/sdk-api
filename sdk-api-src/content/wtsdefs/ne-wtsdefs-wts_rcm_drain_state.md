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

# WTS_RCM_DRAIN_STATE enumeration


## -description


Contains information about the drain state of the Remote Desktop Session Host (RD Session Host) server. A server in drain mode will not accept new connections, but it will reconnect users to existing sessions.


## -enum-fields




### -field WTS_DRAIN_STATE_NONE

There has been no change in the drain state.


### -field WTS_DRAIN_IN_DRAIN

The server is in drain mode, or it is entering drain mode. (It is not accepting new connections.)


### -field WTS_DRAIN_NOT_IN_DRAIN

The server is not in drain mode, or it is exiting drain mode. (It is accepting new connections.)


## -remarks



This enumeration type is used by the <a href="https://msdn.microsoft.com/5f4469f5-5a64-4292-bbe6-cc030f1421f5">WTS_SERVICE_STATE</a> structure.



