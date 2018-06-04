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

# _TARGET_STATE enumeration


## -description


Indicates the state of a target.


## -enum-fields




### -field TARGET_UNKNOWN

The target state is unknown.


### -field TARGET_INITIALIZING

The target is initializing.


### -field TARGET_RUNNING

The target is running.


### -field TARGET_DOWN

The target is not running. If a resource plug-in calls <b>OnStateChange</b> and the target is in this state, RD Connection Broker will delete the target object from its database.


### -field TARGET_HIBERNATED

The target is hibernated.


### -field TARGET_CHECKED_OUT

The target is checked out.


### -field TARGET_STOPPED

The target is stopped.


### -field TARGET_INVALID


### -field TARGET_STARTING


### -field TARGET_STOPPING


### -field TARGET_MAXSTATE




## -see-also




<a href="https://msdn.microsoft.com/4f4e8883-9f89-47c2-919f-44f4c6e44591">Remote Desktop Virtualization API reference</a>



<a href="https://msdn.microsoft.com/5ba5c4c6-b644-45f7-8942-ee8ea543138d">SetTargetState</a>



<a href="https://msdn.microsoft.com/0913e997-d3f0-44a3-977f-eb760489c43b">TargetState</a>
 

 

