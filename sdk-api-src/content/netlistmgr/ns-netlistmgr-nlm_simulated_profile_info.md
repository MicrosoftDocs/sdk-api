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

# NLM_SIMULATED_PROFILE_INFO structure


## -description


Used to specify values that are used by <a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a> to override current internet connection profile values in an RDP Child Session to support the simulation of specific metered internet connection conditions.


## -struct-fields




### -field ProfileName

Name for the simulated profile.


### -field cost

The network cost. Possible values are defined by <a href="https://msdn.microsoft.com/93541814-A1C3-4C24-BB99-CEE4895F34F8">NLM_CONNECTION_COST</a>.


### -field UsageInMegabytes

The data usage.


### -field DataLimitInMegabytes

The data limit of the plan.


## -see-also




<a href="https://msdn.microsoft.com/65B9DB67-4EE8-40B5-B465-CA425792C62B">Child Sessions (Windows)</a>



<a href="https://msdn.microsoft.com/DD89717F-4BFD-4283-A9F4-A74BB6E8E8D6">ClearSimulatedProfileInfo</a>



<a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a>
 

 

