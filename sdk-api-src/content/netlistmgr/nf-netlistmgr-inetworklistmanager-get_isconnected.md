---
UID: NF:netlistmgr.INetworkListManager.get_IsConnected
title: INetworkListManager::get_IsConnected
author: windows-sdk-content
description: The get_IsConnected property specifies if the local machine has network connectivity.
old-location: nla\inetworklistmanager_get_isconnected.htm
old-project: NLA
ms.assetid: 51bdec8e-521f-4673-a2ad-07e8995f3905
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: INetworkListManager interface [Network Awareness],get_IsConnected method, INetworkListManager.get_IsConnected, INetworkListManager::get_IsConnected, get_IsConnected, get_IsConnected method [Network Awareness], get_IsConnected method [Network Awareness],INetworkListManager interface, netlistmgr/INetworkListManager::get_IsConnected, nla.inetworklistmanager_get_isconnected
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	INetworkListManager.get_IsConnected
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkListManager::get_IsConnected


## -description


The <b>get_IsConnected</b> property specifies if the local machine has network connectivity.


## -parameters




### -param pbIsConnected [out]

If <b>TRUE</b> ,  the network has at least local connectivity via ipv4 or ipv6 or both. The network may also have internet connectivity.  Thus, the network is connected.



If <b>FALSE</b>, the network does not have local or internet connectivity. The network is not connected.



## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>
 

 

