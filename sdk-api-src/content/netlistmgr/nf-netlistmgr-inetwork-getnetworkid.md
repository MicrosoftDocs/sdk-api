---
UID: NF:netlistmgr.INetwork.GetNetworkId
title: INetwork::GetNetworkId method
author: windows-driver-content
description: The GetNetworkId method returns the unique identifier of a network.
old-location: nla\inetwork_getnetworkid.htm
old-project: NLA
ms.assetid: f2012295-d443-434f-8fe8-b6e38e7cac74
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetNetworkId method [Network Awareness], GetNetworkId method [Network Awareness], INetwork interface, GetNetworkId,INetwork.GetNetworkId, INetwork, INetwork interface [Network Awareness], GetNetworkId method, INetwork::GetNetworkId, netlistmgr/INetwork::GetNetworkId, nla.inetwork_getnetworkid
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
-	INetwork.GetNetworkId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetwork::GetNetworkId method


## -description


The <b>GetNetworkId</b> method returns the unique identifier of a network.


## -parameters




### -param pgdGuidNetworkId [out]

Pointer to a GUID that specifies the network ID.


## -returns



Returns S_OK if the method succeeds.




## -remarks



The caller is responsible for allocating the buffer pointed to by <i>pgdGuidNetworkId</i>. This buffer must be large enough to hold a GUID. 

Calling  <b>GetNetworkId</b> will return S_OK even if the network requested has been deleted.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>
 

 

