---
UID: NF:netlistmgr.INetworkEvents.NetworkPropertyChanged
title: INetworkEvents::NetworkPropertyChanged
author: windows-sdk-content
description: The NetworkPropertyChanged method is called when a network property change is detected.
old-location: nla\inetworkevents_networkpropertychanged.htm
old-project: NLA
ms.assetid: a84f49ee-9efd-450e-a6e6-3f140330a9d0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: INetworkEvents interface [Network Awareness],NetworkPropertyChanged method, INetworkEvents.NetworkPropertyChanged, INetworkEvents::NetworkPropertyChanged, NetworkPropertyChanged, NetworkPropertyChanged method [Network Awareness], NetworkPropertyChanged method [Network Awareness],INetworkEvents interface, netlistmgr/INetworkEvents::NetworkPropertyChanged, nla.inetworkevents_networkpropertychanged
ms.prod: windows
ms.technology: windows-sdk
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
 - INetworkEvents.NetworkPropertyChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkEvents::NetworkPropertyChanged


## -description


The <b>NetworkPropertyChanged</b> method is called when a network property change is detected.


## -parameters




### -param networkId




### -param flags






#### - fFlags [in]


<a href="https://msdn.microsoft.com/04c96793-f6a8-418b-a8d4-65e8df77933c">NLM_NETWORK_PROPERTY_CHANGE</a> enumeration value that specifies the network property that changed.


#### - gdNetworkId [in]

GUID that specifies the network on which this event occurred.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/75cc6efb-dd1b-40b6-84fe-5ba7c244cd72">INetworkEvents</a>



<a href="https://msdn.microsoft.com/04c96793-f6a8-418b-a8d4-65e8df77933c">NLM_NETWORK_PROPERTY_CHANGE</a>
 

 

