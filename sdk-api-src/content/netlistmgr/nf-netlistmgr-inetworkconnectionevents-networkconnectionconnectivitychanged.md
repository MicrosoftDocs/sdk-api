---
UID: NF:netlistmgr.INetworkConnectionEvents.NetworkConnectionConnectivityChanged
title: INetworkConnectionEvents::NetworkConnectionConnectivityChanged
author: windows-sdk-content
description: The NetworkConnectionConnectivityChanged method notifies a client when connectivity change events occur on a network connection level.
old-location: nla\inetworkconnectionevents_networkconnectionconnectivitychanged.htm
tech.root: NLA
ms.assetid: 0b245a6e-918c-41de-b33e-87723491e900
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: INetworkConnectionEvents interface [Network Awareness],NetworkConnectionConnectivityChanged method, INetworkConnectionEvents.NetworkConnectionConnectivityChanged, INetworkConnectionEvents::NetworkConnectionConnectivityChanged, NetworkConnectionConnectivityChanged, NetworkConnectionConnectivityChanged method [Network Awareness], NetworkConnectionConnectivityChanged method [Network Awareness],INetworkConnectionEvents interface, netlistmgr/INetworkConnectionEvents::NetworkConnectionConnectivityChanged, nla.inetworkconnectionevents_networkconnectionconnectivitychanged
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - INetworkConnectionEvents.NetworkConnectionConnectivityChanged
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
- INetworkConnectionEvents.NetworkConnectionConnectivityChanged
: 
---

# INetworkConnectionEvents::NetworkConnectionConnectivityChanged


## -description


The <b>NetworkConnectionConnectivityChanged</b> method notifies a client when connectivity change events occur on a network connection level.


## -parameters




### -param connectionId [in]

A GUID that identifies the network connection  on which the event occurred.


### -param newConnectivity [in]


<a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a> enumeration value that specifies the new connectivity for this network connection.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/339f23ee-583d-4623-ad43-00b4fd4395ad">INetworkConnectionEvents</a>



<a href="https://msdn.microsoft.com/72d1f049-3c8d-4332-9bf1-9f49b47cd315">NLM_CONNECTIVITY</a>
 

 

