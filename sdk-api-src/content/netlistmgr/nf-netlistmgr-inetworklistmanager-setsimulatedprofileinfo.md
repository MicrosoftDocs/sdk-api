---
UID: NF:netlistmgr.INetworkListManager.SetSimulatedProfileInfo
title: INetworkListManager::SetSimulatedProfileInfo
author: windows-sdk-content
description: The SetSimulatedProfileInfo method applies a specific set of connection profile values to the internet connection profile in support of the simulation of specific metered internet connection conditions.
old-location: nla\inetworklistmanager_setsimulatedprofileinfo.htm
tech.root: NLA
ms.assetid: 168501A6-F8B2-4635-97BB-538994074D2C
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: INetworkListManager interface [Network Awareness],SetSimulatedProfileInfo method, INetworkListManager.SetSimulatedProfileInfo, INetworkListManager::SetSimulatedProfileInfo, SetSimulatedProfileInfo, SetSimulatedProfileInfo method [Network Awareness], SetSimulatedProfileInfo method [Network Awareness],INetworkListManager interface, netlistmgr/INetworkListManager::SetSimulatedProfileInfo, nla.inetworklistmanager_setsimulatedprofileinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkListManager.SetSimulatedProfileInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- netlistmgr.h
: 
- INetworkListManager.SetSimulatedProfileInfo
: 
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
 

 

