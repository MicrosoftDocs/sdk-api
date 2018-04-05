---
UID: NF:netlistmgr.INetworkEvents.NetworkDeleted
title: INetworkEvents::NetworkDeleted method
author: windows-driver-content
description: The NetworkDeleted method is called when a network is deleted.
old-location: nla\inetworkevents_networkdeleted.htm
old-project: NLA
ms.assetid: ae54cc29-6da8-405d-92f9-654239150dd0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: INetworkEvents, INetworkEvents interface [Network Awareness], NetworkDeleted method, INetworkEvents::NetworkDeleted, NetworkDeleted method [Network Awareness], NetworkDeleted method [Network Awareness], INetworkEvents interface, NetworkDeleted,INetworkEvents.NetworkDeleted, netlistmgr/INetworkEvents::NetworkDeleted, nla.inetworkevents_networkdeleted
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	INetworkEvents.NetworkDeleted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# INetworkEvents::NetworkDeleted method


## -description


The <b>NetworkDeleted</b> method is called when a network is deleted.


## -parameters




### -param networkId






#### - gdNetworkId [in]

GUID that contains the network ID of the network that was deleted.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/75cc6efb-dd1b-40b6-84fe-5ba7c244cd72">INetworkEvents</a>
 

 

