---
UID: NF:netlistmgr.INetwork.GetConnectivity
title: INetwork::GetConnectivity (netlistmgr.h)
description: The GetConnectivity method returns the connectivity state of the network.
helpviewer_keywords: ["GetConnectivity","GetConnectivity method [Network Awareness]","GetConnectivity method [Network Awareness]","INetwork interface","INetwork interface [Network Awareness]","GetConnectivity method","INetwork.GetConnectivity","INetwork::GetConnectivity","netlistmgr/INetwork::GetConnectivity","nla.inetwork_getconnectivity"]
old-location: nla\inetwork_getconnectivity.htm
tech.root: nla
ms.assetid: 04191757-7d9f-4211-a311-4863d62bd0a5
ms.date: 12/05/2018
ms.keywords: GetConnectivity, GetConnectivity method [Network Awareness], GetConnectivity method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetConnectivity method, INetwork.GetConnectivity, INetwork::GetConnectivity, netlistmgr/INetwork::GetConnectivity, nla.inetwork_getconnectivity
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
 - INetwork::GetConnectivity
 - netlistmgr/INetwork::GetConnectivity
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
 - INetwork.GetConnectivity
---

# INetwork::GetConnectivity


## -description

The <b>GetConnectivity</b> method returns the connectivity state of the network.

## -parameters

### -param pConnectivity [out]

Pointer to a <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a> enumeration value that contains a bitmask  that specifies the connectivity state of this network.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>



<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a>