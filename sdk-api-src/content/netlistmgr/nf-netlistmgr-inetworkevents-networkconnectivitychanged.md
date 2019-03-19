---
UID: NF:netlistmgr.INetworkEvents.NetworkConnectivityChanged
title: INetworkEvents::NetworkConnectivityChanged (netlistmgr.h)
author: windows-sdk-content
description: The NetworkConnectivityChanged method is called when network connectivity related changes occur.
old-location: nla\inetworkevents_networkconnectivitychanged.htm
tech.root: nla
ms.assetid: adaf3abe-9a8c-45af-bcc7-bcc516ed75ff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetworkEvents interface [Network Awareness],NetworkConnectivityChanged method, INetworkEvents.NetworkConnectivityChanged, INetworkEvents::NetworkConnectivityChanged, NetworkConnectivityChanged, NetworkConnectivityChanged method [Network Awareness], NetworkConnectivityChanged method [Network Awareness],INetworkEvents interface, netlistmgr/INetworkEvents::NetworkConnectivityChanged, nla.inetworkevents_networkconnectivitychanged
ms.topic: method
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
 - INetworkEvents.NetworkConnectivityChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetworkEvents::NetworkConnectivityChanged


## -description


The <b>NetworkConnectivityChanged</b> method is called when network connectivity related changes occur.


## -parameters




### -param networkId [in]

 A <b>GUID</b> that specifies the new network that was added.


### -param newConnectivity [in]


<a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a> enumeration value that contains the new connectivity of this network.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/75cc6efb-dd1b-40b6-84fe-5ba7c244cd72">INetworkEvents</a>



<a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a>
 

 

