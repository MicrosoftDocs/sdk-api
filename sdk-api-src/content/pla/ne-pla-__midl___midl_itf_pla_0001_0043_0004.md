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

# __MIDL___MIDL_itf_pla_0001_0043_0004 enumeration


## -description


Defines the running status of the data collector set.


## -enum-fields




### -field plaStopped

The data collector set is not running.


### -field plaRunning

The data collector set is running.


### -field plaCompiling

The data collector set is performing data management. A running data collector set will transition from <b>plaRunning</b> to <b>plaCompiling</b> if the data manager is enabled.


### -field plaPending

The data collector has been set to run, but the service has not started it yet.  Only computers that run operating systems prior to Windows Vista report this status.


### -field plaUndefined

Cannot determine the status but no error has occurred. Typically, this status is set for autologgers.


## -see-also




<a href="https://msdn.microsoft.com/d957d34d-5455-486a-bd54-28afd7e6f979">IDataCollectorSet::Status</a>
 

 

