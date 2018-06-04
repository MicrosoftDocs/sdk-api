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

# _tagSYNCMGRFLAG enumeration


## -description


The <b>SYNCMGRFLAG</b> enumeration values are used in the <a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a> method to indicate how the synchronization event was initiated.


## -enum-fields




### -field SYNCMGRFLAG_CONNECT

Synchronization was initiated by a network connect event.


### -field SYNCMGRFLAG_PENDINGDISCONNECT

Synchronization was initiated by a pending network disconnect event.


### -field SYNCMGRFLAG_MANUAL

Synchronization was initiated manually by the end user.


### -field SYNCMGRFLAG_IDLE

Synchronization was programmatically invoked.


### -field SYNCMGRFLAG_INVOKE

Synchronization was programmatically invoked.


### -field SYNCMGRFLAG_SCHEDULED

Synchronization was initiated by a scheduled update event.


### -field SYNCMGRFLAG_EVENTMASK

Synchronization mask value.


### -field SYNCMGRFLAG_SETTINGS

Synchronization was initiated for configuration purposes only in the <b>System Properties</b> dialog box.


### -field SYNCMGRFLAG_MAYBOTHERUSER

Interaction with the user is permitted. The application is allowed to show user interface elements and interact with the user. If this flag is not set, the application must not display any user interface elements other than using the <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a> interface. If an application cannot complete the synchronization without displaying user interface elements and this flag is not set, the application fails the synchronization.


## -see-also




<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a>
 

 

