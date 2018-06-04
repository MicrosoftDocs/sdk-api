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

# _RM_APP_STATUS enumeration


## -description


Describes the current status of an application that is acted upon by the Restart Manager.


## -enum-fields




### -field RmStatusUnknown

The application is in a state that is not described by any other enumerated state.


### -field RmStatusRunning

The application is currently running.


### -field RmStatusStopped

The Restart Manager has stopped the application.


### -field RmStatusStoppedOther

An action outside the Restart Manager has stopped the application.


### -field RmStatusRestarted

The Restart Manager has restarted the application.


### -field RmStatusErrorOnStop

The Restart Manager encountered an error when stopping the application.


### -field RmStatusErrorOnRestart

The Restart Manager encountered an error when restarting the application.


### -field RmStatusShutdownMasked

Shutdown is masked by a filter.


### -field RmStatusRestartMasked

Restart is masked by a filter.


## -remarks



The constants  of <b>RM_APP_STATUS</b> can be combined with OR operators. The combination describes the history of actions taken by Restart Manager on the application.




## -see-also




<a href="https://msdn.microsoft.com/27e593f9-8ff0-4de4-87ca-7fa5f324468a">RM_PROCESS_INFO</a>
 

 

