---
UID: NF:netlistmgr.INetwork.GetNetworkConnections
title: INetwork::GetNetworkConnections
author: windows-sdk-content
description: The GetNetworkConnections method returns an enumeration of all network connections for a network. A network can have multiple connections to it from different interfaces or different links from the same interface.
old-location: nla\inetwork_getnetworkconnections.htm
old-project: nla
ms.assetid: cc599537-3c31-4674-81d0-608cadae3e61
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetNetworkConnections, GetNetworkConnections method [Network Awareness], GetNetworkConnections method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetNetworkConnections method, INetwork.GetNetworkConnections, INetwork::GetNetworkConnections, netlistmgr/INetwork::GetNetworkConnections, nla.inetwork_getnetworkconnections
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
 - INetwork.GetNetworkConnections
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetwork::GetNetworkConnections


## -description


The <b>GetNetworkConnections</b> method returns an enumeration of all network connections for a network. A network can have multiple connections to it from different interfaces or different links from the same interface.


## -parameters




### -param ppEnumNetworkConnection [out]

Pointer to an <a href="https://msdn.microsoft.com/f7e69ede-c567-4285-a017-096c94fb3fe4">IEnumNetworkConnections</a> interface instance that enumerates the list of local connections to this network.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>
 

 

