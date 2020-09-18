---
UID: NF:netlistmgr.INetworkListManager.GetConnectivity
title: INetworkListManager::GetConnectivity (netlistmgr.h)
description: The GetConnectivity method returns the overall connectivity state of the machine.
helpviewer_keywords: ["GetConnectivity","GetConnectivity method [Network Awareness]","GetConnectivity method [Network Awareness]","INetworkListManager interface","INetworkListManager interface [Network Awareness]","GetConnectivity method","INetworkListManager.GetConnectivity","INetworkListManager::GetConnectivity","netlistmgr/INetworkListManager::GetConnectivity","nla.inetworklistmanager_getconnectivity"]
old-location: nla\inetworklistmanager_getconnectivity.htm
tech.root: nla
ms.assetid: 4695554a-2f8b-4d2e-b3ff-ec22c43387d6
ms.date: 12/05/2018
ms.keywords: GetConnectivity, GetConnectivity method [Network Awareness], GetConnectivity method [Network Awareness],INetworkListManager interface, INetworkListManager interface [Network Awareness],GetConnectivity method, INetworkListManager.GetConnectivity, INetworkListManager::GetConnectivity, netlistmgr/INetworkListManager::GetConnectivity, nla.inetworklistmanager_getconnectivity
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - INetworkListManager::GetConnectivity
 - netlistmgr/INetworkListManager::GetConnectivity
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
 - INetworkListManager.GetConnectivity
---

# INetworkListManager::GetConnectivity


## -description

The <b>GetConnectivity</b> method returns the overall connectivity state of the machine.

## -parameters

### -param pConnectivity [out]

Pointer to an <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a> enumeration value that contains a bitmask that specifies the network connectivity of this machine.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>