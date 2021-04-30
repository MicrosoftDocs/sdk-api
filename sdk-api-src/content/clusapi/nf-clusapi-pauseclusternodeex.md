---
UID: NF:clusapi.PauseClusterNodeEx
title: PauseClusterNodeEx function (clusapi.h)
description: Requests that a node temporarily suspends its cluster activity.
helpviewer_keywords: ["PCLUSAPI_PAUSE_CLUSTER_NODE_EX","PCLUSAPI_PAUSE_CLUSTER_NODE_EX function [Failover Cluster]","PauseClusterNodeEx","PauseClusterNodeEx function [Failover Cluster]","clusapi/PCLUSAPI_PAUSE_CLUSTER_NODE_EX","clusapi/PauseClusterNodeEx","mscs.pauseclusternodeex"]
old-location: mscs\pauseclusternodeex.htm
tech.root: MsCS
ms.assetid: 632C26C2-ED12-40DC-9615-4A09A7E2F7CB
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_PAUSE_CLUSTER_NODE_EX, PCLUSAPI_PAUSE_CLUSTER_NODE_EX function [Failover Cluster], PauseClusterNodeEx, PauseClusterNodeEx function [Failover Cluster], clusapi/PCLUSAPI_PAUSE_CLUSTER_NODE_EX, clusapi/PauseClusterNodeEx, mscs.pauseclusternodeex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PauseClusterNodeEx
 - clusapi/PauseClusterNodeEx
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - PauseClusterNodeEx
---

# PauseClusterNodeEx function


## -description

Requests that a 
node temporarily suspends its cluster activity.

## -parameters

### -param hNode [in]

A handle to the node to suspend.

### -param bDrainNode [in]

<b>TRUE</b> to drain the node; otherwise <b>FALSE</b>.

### -param dwPauseFlags [in] [in]

One of the following flags:
- CLUSAPI_NODE_PAUSE_REMAIN_ON_PAUSED_NODE_ON_MOVE_ERROR  0x00000001
- CLUSAPI_NODE_AVOID_PLACEMENT                            0x00000002
- CLUSAPI_NODE_PAUSE_RETRY_DRAIN_ON_FAILURE  0x00000004

### -param hNodeDrainTarget [in, optional] [in, optional]

The node drain topic.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>