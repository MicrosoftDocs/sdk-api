---
UID: NF:netlistmgr.INetworkCostManagerEvents.DataPlanStatusChanged
title: INetworkCostManagerEvents::DataPlanStatusChanged
author: windows-sdk-content
description: DataPlanStatusChanged method is called to indicate a change to the status of a data plan associated with either a connection used for machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.
old-location: nla\inetworkcostmanagerevents_dataplanstatuschanged.htm
old-project: NLA
ms.assetid: A9908F22-A9E9-4C05-A434-57D0C433EA3E
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DataPlanStatusChanged, DataPlanStatusChanged method [Network Awareness], DataPlanStatusChanged method [Network Awareness],INetworkCostManagerEvents interface, INetworkCostManagerEvents interface [Network Awareness],DataPlanStatusChanged method, INetworkCostManagerEvents.DataPlanStatusChanged, INetworkCostManagerEvents::DataPlanStatusChanged, netlistmgr/INetworkCostManagerEvents::DataPlanStatusChanged, nla.inetworkcostmanagerevents_dataplanstatuschanged
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
req.typenames: NLM_NETWORK_PROPERTY_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Netlistmgr.h
api_name:
-	INetworkCostManagerEvents.DataPlanStatusChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetworkCostManagerEvents::DataPlanStatusChanged


## -description


The <b>DataPlanStatusChanged</b> method is called to indicate a change to the status of a data plan associated with either a connection used for  machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.


## -parameters




### -param pDestAddr

An <a href="https://msdn.microsoft.com/BEAF672C-F9B3-4544-878B-BBCF96F502C6">NLM_SOCKADDR</a> structure containing an IPv4/IPv6 address that identifies the destination for which the event occurred. If <i>destAddr</i> is NULL, the change is a machine-wide Internet connectivity change.


## -returns



Returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/A8F4194E-6E9A-4173-8F88-FC2923B11CF0">INetworkCostManagerEvents</a>
 

 

