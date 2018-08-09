---
UID: NF:netlistmgr.INetworkCostManagerEvents.CostChanged
title: INetworkCostManagerEvents::CostChanged
author: windows-sdk-content
description: CostChanged method is called to indicates a cost change for either machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.
old-location: nla\inetworkcostmanagerevents_costchanged.htm
old-project: nla
ms.assetid: 39262F6A-9701-4917-BBDF-1BAC201585D4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CostChanged, CostChanged method [Network Awareness], CostChanged method [Network Awareness],INetworkCostManagerEvents interface, INetworkCostManagerEvents interface [Network Awareness],CostChanged method, INetworkCostManagerEvents.CostChanged, INetworkCostManagerEvents::CostChanged, netlistmgr/INetworkCostManagerEvents::CostChanged, nla.inetworkcostmanagerevents_costchanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - INetworkCostManagerEvents.CostChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkCostManagerEvents::CostChanged


## -description


The <b>CostChanged</b> method is called to indicates a cost change for either machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.


## -parameters




### -param newCost [in]

A DWORD that represents the new cost of the connection. The lowest 16 bits represent the cost level, and the highest 16 bits represent the flags. Possible values are defined by the <a href="https://msdn.microsoft.com/93541814-A1C3-4C24-BB99-CEE4895F34F8">NLM_CONNECTION_COST</a> enumeration.


### -param pDestAddr [in]

An <a href="https://msdn.microsoft.com/BEAF672C-F9B3-4544-878B-BBCF96F502C6">NLM_SOCKADDR</a> structure containing an IPv4/IPv6 address that identifies the destination on which the event occurred. If <i>destAddr</i> is NULL, the change is a machine-wide Internet connectivity change.


## -returns



Returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/A8F4194E-6E9A-4173-8F88-FC2923B11CF0">INetworkCostManagerEvents</a>
 

 

