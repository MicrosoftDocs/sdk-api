---
UID: NS:netlistmgr.NLM_SIMULATED_PROFILE_INFO
title: NLM_SIMULATED_PROFILE_INFO
author: windows-sdk-content
description: Used to specify values that are used by SetSimulatedProfileInfo to override current internet connection profile values in an RDP Child Session to support the simulation of specific metered internet connection conditions.
old-location: nla\nlm_simulated_profile_info.htm
tech.root: nla
ms.assetid: 1DC80EB0-E63A-4352-8269-D795E1573851
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: NLM_SIMULATED_PROFILE_INFO, NLM_SIMULATED_PROFILE_INFO structure [Network Awareness], PNLM_SIMULATED_PROFILE_INFO, PNLM_SIMULATED_PROFILE_INFO structure pointer [Network Awareness], netlistmgr/NLM_SIMULATED_PROFILE_INFO, netlistmgr/PNLM_SIMULATED_PROFILE_INFO, nla.nlm_simulated_profile_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netlistmgr.h
api_name:
 - NLM_SIMULATED_PROFILE_INFO
product: Windows
targetos: Windows
req.typenames: NLM_SIMULATED_PROFILE_INFO
req.redist: 
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
 

 

