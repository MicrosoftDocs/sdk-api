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

# _PROCESSOR_POWER_POLICY_INFO structure


## -description


Contains information about processor C-state policy settings. This structure is part of the 
<a href="https://msdn.microsoft.com/ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a">PROCESSOR_POWER_POLICY</a> structure.


## -struct-fields




### -field TimeCheck

The time that must expire before promotion or demotion is considered, in microseconds.


### -field DemoteLimit

The minimum amount of time that must be spent in the idle loop to avoid demotion, in microseconds.


### -field PromoteLimit

The time that must be exceeded to cause promotion to a deeper idle state, in microseconds.


### -field DemotePercent

The value that scales the threshold at which the power policy manager decreases the performance of the processor, expressed as a percentage.


### -field PromotePercent

The value that scales the threshold at which the power policy manager increases the performance of the processor, expressed as a percentage.


### -field Spare

Reserved.


### -field AllowDemotion

When set, allows the kernel power policy manager to demote from the current state.


### -field AllowPromotion

When set, allows the kernel power policy manager to promote from the current state.


### -field Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/ea1eae62-26b4-4f5d-a9ca-0a7bb463b90a">PROCESSOR_POWER_POLICY</a>
 

 

