---
UID: NF:netlistmgr.INetworkConnection.GetConnectionId
title: INetworkConnection::GetConnectionId method
author: windows-driver-content
description: The GetConnectionID method returns the Connection ID associated with this network connection.
old-location: nla\inetworkconnection_getconnectionid.htm
old-project: NLA
ms.assetid: c8619fd1-2764-4f20-a258-fb4368e448b7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetConnectionId method [Network Awareness], GetConnectionId method [Network Awareness], INetworkConnection interface, GetConnectionId,INetworkConnection.GetConnectionId, INetworkConnection, INetworkConnection interface [Network Awareness], GetConnectionId method, INetworkConnection::GetConnectionId, netlistmgr/INetworkConnection::GetConnectionId, nla.inetworkconnection_getconnectionid
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
-	INetworkConnection.GetConnectionId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# INetworkConnection::GetConnectionId method


## -description


The <a href="https://msdn.microsoft.com/69711dea-e0dd-4c1e-a83f-1f06d4259b35">GetConnectionID</a> method returns the Connection ID associated with this network connection.


## -parameters




### -param pgdConnectionId [out]

Pointer to a <b>GUID</b> that specifies the Connection ID associated with this network connection. 


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/666761b5-0146-438d-9986-ecce3b45b5ff">INetworkConnection</a>
 

 

