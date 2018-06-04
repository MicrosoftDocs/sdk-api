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

# _RM_REBOOT_REASON enumeration


## -description


Describes the reasons a restart of the system is needed.


## -enum-fields




### -field RmRebootReasonNone

A system restart is not required.


### -field RmRebootReasonPermissionDenied

The current user does not have
                                            sufficient privileges to shut down one or more processes.


### -field RmRebootReasonSessionMismatch

One or more processes are
                                            running in another Terminal Services session.


### -field RmRebootReasonCriticalProcess

A system restart is needed because one or more processes to be shut down are critical processes.


### -field RmRebootReasonCriticalService

A system restart is needed because one or more services to be shut down are critical services.


### -field RmRebootReasonDetectedSelf

A system restart is needed because the current process must be shut down.


## -see-also




<a href="https://msdn.microsoft.com/de4feea4-2b45-4430-a4b3-8ca26c455e42">RmGetList</a>
 

 

