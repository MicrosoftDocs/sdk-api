---
UID: NF:netlistmgr.INetworkCostManagerEvents.DataPlanStatusChanged
title: INetworkCostManagerEvents::DataPlanStatusChanged (netlistmgr.h)
description: DataPlanStatusChanged method is called to indicate a change to the status of a data plan associated with either a connection used for machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.
helpviewer_keywords: ["DataPlanStatusChanged","DataPlanStatusChanged method [Network Awareness]","DataPlanStatusChanged method [Network Awareness]","INetworkCostManagerEvents interface","INetworkCostManagerEvents interface [Network Awareness]","DataPlanStatusChanged method","INetworkCostManagerEvents.DataPlanStatusChanged","INetworkCostManagerEvents::DataPlanStatusChanged","netlistmgr/INetworkCostManagerEvents::DataPlanStatusChanged","nla.inetworkcostmanagerevents_dataplanstatuschanged"]
old-location: nla\inetworkcostmanagerevents_dataplanstatuschanged.htm
tech.root: nla
ms.assetid: A9908F22-A9E9-4C05-A434-57D0C433EA3E
ms.date: 12/05/2018
ms.keywords: DataPlanStatusChanged, DataPlanStatusChanged method [Network Awareness], DataPlanStatusChanged method [Network Awareness],INetworkCostManagerEvents interface, INetworkCostManagerEvents interface [Network Awareness],DataPlanStatusChanged method, INetworkCostManagerEvents.DataPlanStatusChanged, INetworkCostManagerEvents::DataPlanStatusChanged, netlistmgr/INetworkCostManagerEvents::DataPlanStatusChanged, nla.inetworkcostmanagerevents_dataplanstatuschanged
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetworkCostManagerEvents::DataPlanStatusChanged
 - netlistmgr/INetworkCostManagerEvents::DataPlanStatusChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkCostManagerEvents.DataPlanStatusChanged
---

# INetworkCostManagerEvents::DataPlanStatusChanged


## -description

The <b>DataPlanStatusChanged</b> method is called to indicate a change to the status of a data plan associated with either a connection used for  machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.

## -parameters

### -param pDestAddr

An <a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_sockaddr">NLM_SOCKADDR</a> structure containing an IPv4/IPv6 address that identifies the destination for which the event occurred. If <i>destAddr</i> is NULL, the change is a machine-wide Internet connectivity change.

## -returns

Returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkcostmanagerevents">INetworkCostManagerEvents</a>