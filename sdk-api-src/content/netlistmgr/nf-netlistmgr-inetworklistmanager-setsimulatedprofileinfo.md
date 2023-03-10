---
UID: NF:netlistmgr.INetworkListManager.SetSimulatedProfileInfo
title: INetworkListManager::SetSimulatedProfileInfo (netlistmgr.h)
description: The SetSimulatedProfileInfo method applies a specific set of connection profile values to the internet connection profile in support of the simulation of specific metered internet connection conditions.
helpviewer_keywords: ["INetworkListManager interface [Network Awareness]","SetSimulatedProfileInfo method","INetworkListManager.SetSimulatedProfileInfo","INetworkListManager::SetSimulatedProfileInfo","SetSimulatedProfileInfo","SetSimulatedProfileInfo method [Network Awareness]","SetSimulatedProfileInfo method [Network Awareness]","INetworkListManager interface","netlistmgr/INetworkListManager::SetSimulatedProfileInfo","nla.inetworklistmanager_setsimulatedprofileinfo"]
old-location: nla\inetworklistmanager_setsimulatedprofileinfo.htm
tech.root: nla
ms.assetid: 168501A6-F8B2-4635-97BB-538994074D2C
ms.date: 12/05/2018
ms.keywords: INetworkListManager interface [Network Awareness],SetSimulatedProfileInfo method, INetworkListManager.SetSimulatedProfileInfo, INetworkListManager::SetSimulatedProfileInfo, SetSimulatedProfileInfo, SetSimulatedProfileInfo method [Network Awareness], SetSimulatedProfileInfo method [Network Awareness],INetworkListManager interface, netlistmgr/INetworkListManager::SetSimulatedProfileInfo, nla.inetworklistmanager_setsimulatedprofileinfo
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
 - INetworkListManager::SetSimulatedProfileInfo
 - netlistmgr/INetworkListManager::SetSimulatedProfileInfo
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
 - INetworkListManager.SetSimulatedProfileInfo
---

# INetworkListManager::SetSimulatedProfileInfo


## -description

The <b>SetSimulatedProfileInfo</b> method applies a specific set of connection profile values to the internet connection profile in support of the simulation of specific metered internet connection conditions.

The simulation only applies in an RDP Child Session and does not affect the primary user session.  The simulated internet connection profile is returned via the Windows Runtime API <a href="/uwp/api/windows.networking.connectivity.networkinformation.getinternetconnectionprofile">GetInternetConnectionProfile</a>.

## -parameters

### -param pSimulatedInfo

Specific connection profile values to simulate on the current internet connection profile  when calling <a href="/uwp/api/windows.networking.connectivity.networkinformation.getinternetconnectionprofile">GetInternetConnectionProfile</a> from an RDP Child Session

## -returns

Returns S_OK on success.

## -see-also

<a href="/windows/desktop/TermServ/child-sessions">Child Sessions (Windows)</a>



<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-clearsimulatedprofileinfo">ClearSimulatedProfileInfo</a>



<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>



<a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_simulated_profile_info">NLM_SIMULATED_PROFILE_INFO</a>