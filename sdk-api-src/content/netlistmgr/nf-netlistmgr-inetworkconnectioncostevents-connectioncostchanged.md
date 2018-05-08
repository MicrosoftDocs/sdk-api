---
UID: NF:netlistmgr.INetworkConnectionCostEvents.ConnectionCostChanged
title: INetworkConnectionCostEvents::ConnectionCostChanged
author: windows-driver-content
description: ConnectionCostChanged method notifies an application of a network cost change for a connection.
old-location: nla\inetworkconnectioncostevents_connectioncostchanged.htm
old-project: NLA
ms.assetid: 85D0BF59-3E06-4978-8400-71FD7BF990C9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ConnectionCostChanged, ConnectionCostChanged method [Network Awareness], ConnectionCostChanged method [Network Awareness],INetworkConnectionCostEvents interface, INetworkConnectionCostEvents interface [Network Awareness],ConnectionCostChanged method, INetworkConnectionCostEvents.ConnectionCostChanged, INetworkConnectionCostEvents::ConnectionCostChanged, netlistmgr/INetworkConnectionCostEvents::ConnectionCostChanged, nla.inetworkconnectioncostevents_connectioncostchanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
-	INetworkConnectionCostEvents.ConnectionCostChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetworkConnectionCostEvents::ConnectionCostChanged


## -description


The <b>ConnectionCostChanged</b> method notifies an application of a network cost change for a connection.


## -parameters




### -param connectionId [in]

A unique ID  that identifies the connection on which the cost change event occurred.


### -param newCost [in]

A DWORD value that represents the new cost of the connection. The lowest 16 bits represent the cost level, and the highest 16 bits represent the flags. Possible values are defined by the <a href="https://msdn.microsoft.com/93541814-A1C3-4C24-BB99-CEE4895F34F8">NLM_CONNECTION_COST</a> enumeration.


## -returns



This method returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/ABFE73E5-CB9E-4077-81D2-DD0FB39F4EC5">INetworkConnectionCostEvents</a>
 

 

