---
UID: NF:netlistmgr.INetworkListManager.ClearSimulatedProfileInfo
title: INetworkListManager::ClearSimulatedProfileInfo
author: windows-sdk-content
description: Clears the connection profile values previously applied to the internet connection profile by SetSimulatedProfileInfo. The next internet connection query, via GetInternetConnectionProfile, will use system information.
old-location: nla\inetworklistmanager_clearsimulatedprofileinfo.htm
old-project: NLA
ms.assetid: DD89717F-4BFD-4283-A9F4-A74BB6E8E8D6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ClearSimulatedProfileInfo, ClearSimulatedProfileInfo method [Network Awareness], ClearSimulatedProfileInfo method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],ClearSimulatedProfileInfo method, INetworkListManager.ClearSimulatedProfileInfo, INetworkListManager::ClearSimulatedProfileInfo, netlistmgr/INetworkListManager::ClearSimulatedProfileInfo, nla.inetworklistmanager_clearsimulatedprofileinfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkListManager.ClearSimulatedProfileInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkListManager::ClearSimulatedProfileInfo


## -description


Clears the connection profile values previously applied to the internet connection profile by <a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a>. The next internet connection query, via <a href="https://msdn.microsoft.com/30d85516-1150-45a1-8941-a299019897d6">GetInternetConnectionProfile</a>, will use system information.


## -parameters






## -returns



Returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>



<a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a>
 

 

