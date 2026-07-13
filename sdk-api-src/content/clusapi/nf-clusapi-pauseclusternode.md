---
UID: NF:clusapi.PauseClusterNode
title: PauseClusterNode function (clusapi.h)
description: Requests that a node temporarily suspend its cluster activity. The PCLUSAPI_PAUSE_CLUSTER_NODE type defines a pointer to this function.
helpviewer_keywords: ["PCLUSAPI_PAUSE_CLUSTER_NODE","PCLUSAPI_PAUSE_CLUSTER_NODE function [Failover Cluster]","PauseClusterNode","PauseClusterNode function [Failover Cluster]","_wolf_pauseclusternode","clusapi/PCLUSAPI_PAUSE_CLUSTER_NODE","clusapi/PauseClusterNode","mscs.pauseclusternode"]
old-location: mscs\pauseclusternode.htm
tech.root: MsCS
ms.assetid: 23b4ff74-f72f-4227-9b69-ff36fa6ed55b
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_PAUSE_CLUSTER_NODE, PCLUSAPI_PAUSE_CLUSTER_NODE function [Failover Cluster], PauseClusterNode, PauseClusterNode function [Failover Cluster], _wolf_pauseclusternode, clusapi/PCLUSAPI_PAUSE_CLUSTER_NODE, clusapi/PauseClusterNode, mscs.pauseclusternode
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - PauseClusterNode
 - clusapi/PauseClusterNode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - PauseClusterNode
---

# PauseClusterNode function


## -description

Requests that a  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> temporarily suspend its <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> activity. The <b>PCLUSAPI_PAUSE_CLUSTER_NODE</b> type defines a pointer to this function.

## -parameters

### -param hNode [in]

Handle to the node to suspend activity.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

When a node temporarily suspends its cluster activity,  <a href="/previous-versions/windows/desktop/mscs/groups">groups</a> cannot be moved to the node. Furthermore, groups that would normally fail over to the node cannot do so when it is in the paused state.

Groups that are owned by a paused node remain owned by the node. A paused node's groups and resources can be taken offline, but they cannot be brought online. Because the paused state is persistent, a paused node that is rebooted continues to be paused when it comes back up.

A paused node is said to be in the <b>ClusterNodePaused</b> state (see  <a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodestate">GetClusterNodeState</a>). To resume a node's cluster activity, use the  <a href="/windows/desktop/api/clusapi/nf-clusapi-resumeclusternode">ResumeClusterNode</a> function.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusternodestate">GetClusterNodeState</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-resumeclusternode">ResumeClusterNode</a>