---
UID: NF:netlistmgr.INetworkConnectionCostEvents.ConnectionDataPlanStatusChanged
title: INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged (netlistmgr.h)
description: ConnectionDataPlanStatusChanged method notifies an application of a data plan status change on a connection.
helpviewer_keywords: ["ConnectionDataPlanStatusChanged","ConnectionDataPlanStatusChanged method [Network Awareness]","ConnectionDataPlanStatusChanged method [Network Awareness]","INetworkConnectionCostEvents interface","INetworkConnectionCostEvents interface [Network Awareness]","ConnectionDataPlanStatusChanged method","INetworkConnectionCostEvents.ConnectionDataPlanStatusChanged","INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged","netlistmgr/INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged","nla.inetworkconnectioncostevents_connectiondataplanstatuschanged"]
old-location: nla\inetworkconnectioncostevents_connectiondataplanstatuschanged.htm
tech.root: nla
ms.assetid: F965C648-EC59-40E4-8E8A-FE5A7E8FDAEA
ms.date: 12/05/2018
ms.keywords: ConnectionDataPlanStatusChanged, ConnectionDataPlanStatusChanged method [Network Awareness], ConnectionDataPlanStatusChanged method [Network Awareness],INetworkConnectionCostEvents interface, INetworkConnectionCostEvents interface [Network Awareness],ConnectionDataPlanStatusChanged method, INetworkConnectionCostEvents.ConnectionDataPlanStatusChanged, INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged, netlistmgr/INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged, nla.inetworkconnectioncostevents_connectiondataplanstatuschanged
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged
 - netlistmgr/INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged
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
 - INetworkConnectionCostEvents.ConnectionDataPlanStatusChanged
---

# INetworkConnectionCostEvents::ConnectionDataPlanStatusChanged


## -description

The <b>ConnectionDataPlanStatusChanged</b> method notifies an application of a data plan status change on a connection.

## -parameters

### -param connectionId

A unique ID that identifies the connection on which the data plan status change event occurred.

## -returns

This method returns  S_OK on success.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnectioncostevents">INetworkConnectionCostEvents</a>