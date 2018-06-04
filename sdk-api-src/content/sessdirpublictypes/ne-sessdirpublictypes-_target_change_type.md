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

# _TARGET_CHANGE_TYPE enumeration


## -description


Specifies the type of change that occurred in a target.


## -enum-fields




### -field TARGET_CHANGE_UNSPEC

Unspecified change in the target.


### -field TARGET_EXTERNALIP_CHANGED

The target's external IP address changed.


### -field TARGET_INTERNALIP_CHANGED

The target's internal IP address changed.


### -field TARGET_JOINED

The target was reported to RD Connection Broker.


### -field TARGET_REMOVED

The target was deleted  from the store in RD Connection Broker.


### -field TARGET_STATE_CHANGED

The target's state changed. To determine the current state of the target, check the <a href="https://msdn.microsoft.com/0913e997-d3f0-44a3-977f-eb760489c43b">TargetState</a> property of <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>.


### -field TARGET_IDLE

The target is not hosting any sessions currently.


### -field TARGET_PENDING


### -field TARGET_INUSE


### -field TARGET_PATCH_STATE_CHANGED


### -field TARGET_FARM_MEMBERSHIP_CHANGED




## -see-also




<a href="https://msdn.microsoft.com/d075c7ae-fe86-4547-a980-2b82ea3498c6">NotifyTargetChange</a>



<a href="https://msdn.microsoft.com/4f4e8883-9f89-47c2-919f-44f4c6e44591">Remote Desktop Virtualization API reference</a>
 

 

