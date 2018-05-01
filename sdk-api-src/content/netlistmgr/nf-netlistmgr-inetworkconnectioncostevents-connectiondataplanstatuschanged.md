---
UID: NF:netlistmgr.INetworkConnectionCostEvents.ConnectionDataPlanStatusChanged
title: INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged method
author: windows-driver-content
description: ConnectionDataPlanStatusChanged method notifies an application of a data plan status change on a connection.
old-location: nla\inetworkconnectioncostevents_connectiondataplanstatuschanged.htm
old-project: NLA
ms.assetid: F965C648-EC59-40E4-8E8A-FE5A7E8FDAEA
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ConnectionDataPlanStatusChanged method [Network Awareness], ConnectionDataPlanStatusChanged method [Network Awareness], INetworkConnectionCostEvents interface, ConnectionDataPlanStatusChanged,INetworkConnectionCostEvents.ConnectionDataPlanStatusChanged, INetworkConnectionCostEvents, INetworkConnectionCostEvents interface [Network Awareness], ConnectionDataPlanStatusChanged method, INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged, netlistmgr/INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged, nla.inetworkconnectioncostevents_connectiondataplanstatuschanged
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
-	INetworkConnectionCostEvents.ConnectionDataPlanStatusChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged method


## -description


The <b>ConnectionDataPlanStatusChanged</b> method notifies an application of a data plan status change on a connection.


## -parameters




### -param connectionId

A unique ID that identifies the connection on which the data plan status change event occurred.


## -returns



This method returns  S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/ABFE73E5-CB9E-4077-81D2-DD0FB39F4EC5">INetworkConnectionCostEvents</a>
 

 

