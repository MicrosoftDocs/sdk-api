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

# INetworkListManager::SetSimulatedProfileInfo


## -description


The <b>SetSimulatedProfileInfo</b> method applies a specific set of connection profile values to the internet connection profile in support of the simulation of specific metered internet connection conditions.

The simulation only applies in an RDP Child Session and does not affect the primary user session.  The simulated internet connection profile is returned via the Windows Runtime API <a href="https://msdn.microsoft.com/30d85516-1150-45a1-8941-a299019897d6">GetInternetConnectionProfile</a>.  


## -parameters




### -param pSimulatedInfo

Specific connection profile values to simulate on the current internet connection profile  when calling <a href="https://msdn.microsoft.com/30d85516-1150-45a1-8941-a299019897d6">GetInternetConnectionProfile</a> from an RDP Child Session


## -returns



Returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/65B9DB67-4EE8-40B5-B465-CA425792C62B">Child Sessions (Windows)</a>



<a href="https://msdn.microsoft.com/DD89717F-4BFD-4283-A9F4-A74BB6E8E8D6">ClearSimulatedProfileInfo</a>



<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>



<a href="https://msdn.microsoft.com/1DC80EB0-E63A-4352-8269-D795E1573851">NLM_SIMULATED_PROFILE_INFO</a>
 

 

