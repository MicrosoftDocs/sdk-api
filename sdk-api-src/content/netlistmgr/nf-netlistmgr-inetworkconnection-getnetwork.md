---
UID: NF:netlistmgr.INetworkConnection.GetNetwork
title: INetworkConnection::GetNetwork
author: windows-sdk-content
description: The GetNetwork method returns the network associated with the connection.
old-location: nla\inetworkconnection_getnetwork.htm
old-project: NLA
ms.assetid: 7de83422-58f6-40fc-b26f-074cec550247
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetNetwork, GetNetwork method [Network Awareness], GetNetwork method [Network Awareness],INetworkConnection interface, INetworkConnection interface [Network Awareness],GetNetwork method, INetworkConnection.GetNetwork, INetworkConnection::GetNetwork, netlistmgr/INetworkConnection::GetNetwork, nla.inetworkconnection_getnetwork
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
-	INetworkConnection.GetNetwork
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkConnection::GetNetwork


## -description


The <b>GetNetwork</b> method returns the network associated with the connection.


## -parameters




### -param ppNetwork [out]

Pointer to a pointer that receives an <a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a> interface instance that specifies the network associated with the connection.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a>
 

 

