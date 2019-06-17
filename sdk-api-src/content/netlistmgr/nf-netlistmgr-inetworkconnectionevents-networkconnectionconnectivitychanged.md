---
UID: NF:netlistmgr.INetworkConnectionEvents.NetworkConnectionConnectivityChanged
title: INetworkConnectionEvents::NetworkConnectionConnectivityChanged (netlistmgr.h)
author: windows-sdk-content
description: The NetworkConnectionConnectivityChanged method notifies a client when connectivity change events occur on a network connection level.
old-location: nla\inetworkconnectionevents_networkconnectionconnectivitychanged.htm
tech.root: nla
ms.assetid: 0b245a6e-918c-41de-b33e-87723491e900
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetworkConnectionEvents interface [Network Awareness],NetworkConnectionConnectivityChanged method, INetworkConnectionEvents.NetworkConnectionConnectivityChanged, INetworkConnectionEvents::NetworkConnectionConnectivityChanged, NetworkConnectionConnectivityChanged, NetworkConnectionConnectivityChanged method [Network Awareness], NetworkConnectionConnectivityChanged method [Network Awareness],INetworkConnectionEvents interface, netlistmgr/INetworkConnectionEvents::NetworkConnectionConnectivityChanged, nla.inetworkconnectionevents_networkconnectionconnectivitychanged
ms.topic: method
f1_keywords: ["netlistmgr/INetworkConnectionEvents.NetworkConnectionConnectivityChanged"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkConnectionEvents.NetworkConnectionConnectivityChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetworkConnectionEvents::NetworkConnectionConnectivityChanged


## -description


The <b>NetworkConnectionConnectivityChanged</b> method notifies a client when connectivity change events occur on a network connection level.


## -parameters




### -param connectionId [in]

A GUID that identifies the network connection  on which the event occurred.


### -param newConnectivity [in]


<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a> enumeration value that specifies the new connectivity for this network connection.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnectionevents">INetworkConnectionEvents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a>
 

 

