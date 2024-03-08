---
UID: NF:netlistmgr.INetworkListManagerEvents.ConnectivityChanged
title: INetworkListManagerEvents::ConnectivityChanged (netlistmgr.h)
description: The NetworkConnectivityChanged method is called when network connectivity related changes occur. (INetworkListManagerEvents.ConnectivityChanged)
helpviewer_keywords: ["ConnectivityChanged","ConnectivityChanged method [Network Awareness]","ConnectivityChanged method [Network Awareness]","INetworkListManagerEvents interface","INetworkListManagerEvents interface [Network Awareness]","ConnectivityChanged method","INetworkListManagerEvents.ConnectivityChanged","INetworkListManagerEvents::ConnectivityChanged","netlistmgr/INetworkListManagerEvents::ConnectivityChanged","nla.inetworklistmanagerevents_connectivitychanged"]
old-location: nla\inetworklistmanagerevents_connectivitychanged.htm
tech.root: nla
ms.assetid: 12e15b56-61cd-4fc8-bc0c-9942d40bb2da
ms.date: 12/05/2018
ms.keywords: ConnectivityChanged, ConnectivityChanged method [Network Awareness], ConnectivityChanged method [Network Awareness],INetworkListManagerEvents interface, INetworkListManagerEvents interface [Network Awareness],ConnectivityChanged method, INetworkListManagerEvents.ConnectivityChanged, INetworkListManagerEvents::ConnectivityChanged, netlistmgr/INetworkListManagerEvents::ConnectivityChanged, nla.inetworklistmanagerevents_connectivitychanged
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
 - INetworkListManagerEvents::ConnectivityChanged
 - netlistmgr/INetworkListManagerEvents::ConnectivityChanged
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
 - INetworkListManagerEvents.ConnectivityChanged
---

# INetworkListManagerEvents::ConnectivityChanged


## -description

The <b>NetworkConnectivityChanged</b> method is called when network connectivity related changes occur.

## -parameters

### -param newConnectivity [in]

An <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a> enumeration value that contains the new connectivity settings of the machine.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanagerevents">INetworkListManagerEvents</a>



<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a>
