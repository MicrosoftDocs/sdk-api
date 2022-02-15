---
UID: NF:netlistmgr.INetworkListManager.ClearSimulatedProfileInfo
title: INetworkListManager::ClearSimulatedProfileInfo (netlistmgr.h)
description: Clears the connection profile values previously applied to the internet connection profile by SetSimulatedProfileInfo. The next internet connection query, via GetInternetConnectionProfile, will use system information.
helpviewer_keywords: ["ClearSimulatedProfileInfo","ClearSimulatedProfileInfo method [Network Awareness]","ClearSimulatedProfileInfo method [Network Awareness]","INetworkListManager interface","INetworkListManager interface [Network Awareness]","ClearSimulatedProfileInfo method","INetworkListManager.ClearSimulatedProfileInfo","INetworkListManager::ClearSimulatedProfileInfo","netlistmgr/INetworkListManager::ClearSimulatedProfileInfo","nla.inetworklistmanager_clearsimulatedprofileinfo"]
old-location: nla\inetworklistmanager_clearsimulatedprofileinfo.htm
tech.root: nla
ms.assetid: DD89717F-4BFD-4283-A9F4-A74BB6E8E8D6
ms.date: 12/05/2018
ms.keywords: ClearSimulatedProfileInfo, ClearSimulatedProfileInfo method [Network Awareness], ClearSimulatedProfileInfo method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],ClearSimulatedProfileInfo method, INetworkListManager.ClearSimulatedProfileInfo, INetworkListManager::ClearSimulatedProfileInfo, netlistmgr/INetworkListManager::ClearSimulatedProfileInfo, nla.inetworklistmanager_clearsimulatedprofileinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetworkListManager::ClearSimulatedProfileInfo
 - netlistmgr/INetworkListManager::ClearSimulatedProfileInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkListManager.ClearSimulatedProfileInfo
---

# INetworkListManager::ClearSimulatedProfileInfo


## -description

Clears the connection profile values previously applied to the internet connection profile by <a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-setsimulatedprofileinfo">SetSimulatedProfileInfo</a>. The next internet connection query, via <a href="/uwp/api/windows.networking.connectivity.networkinformation.getinternetconnectionprofile">GetInternetConnectionProfile</a>, will use system information.



## -returns

Returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>



<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-setsimulatedprofileinfo">SetSimulatedProfileInfo</a>
