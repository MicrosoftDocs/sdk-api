---
UID: NC:clusapi.PCLUSTER_UPGRADE_PROGRESS_CALLBACK
title: PCLUSTER_UPGRADE_PROGRESS_CALLBACK (clusapi.h)
description: Retrieves status information for a rolling upgrade of the operating system on a cluster. PCLUSTER_UPGRADE_PROGRESS_CALLBACK type defines a pointer to this function.
helpviewer_keywords: ["ClusterUpgradeProgressCallback","ClusterUpgradeProgressCallback callback","ClusterUpgradeProgressCallback callback function [Failover Cluster]","PCLUSTER_UPGRADE_PROGRESS_CALLBACK","PCLUSTER_UPGRADE_PROGRESS_CALLBACK callback function [Failover Cluster]","clusapi/ClusterUpgradeProgressCallback","clusapi/PCLUSTER_UPGRADE_PROGRESS_CALLBACK","mscs.clusterupgradeprogresscallback"]
old-location: mscs\clusterupgradeprogresscallback.htm
tech.root: MsCS
ms.assetid: EE803D8C-3EFD-414F-8E38-65A1DFA8079B
ms.date: 12/05/2018
ms.keywords: ClusterUpgradeProgressCallback, ClusterUpgradeProgressCallback callback, ClusterUpgradeProgressCallback callback function [Failover Cluster], PCLUSTER_UPGRADE_PROGRESS_CALLBACK, PCLUSTER_UPGRADE_PROGRESS_CALLBACK callback function [Failover Cluster], clusapi/ClusterUpgradeProgressCallback, clusapi/PCLUSTER_UPGRADE_PROGRESS_CALLBACK, mscs.clusterupgradeprogresscallback
req.header: clusapi.h
req.include-header: CluAPI.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - PCLUSTER_UPGRADE_PROGRESS_CALLBACK
 - clusapi/PCLUSTER_UPGRADE_PROGRESS_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - clusapi.h
api_name:
 - ClusterUpgradeProgressCallback
---

# PCLUSTER_UPGRADE_PROGRESS_CALLBACK callback function


## -description

Retrieves status information for a rolling upgrade of the operating system on a cluster. <b>PCLUSTER_UPGRADE_PROGRESS_CALLBACK</b> type defines a pointer to this function.

## -parameters

### -param pvCallbackArg

A pointer to the arguments.

### -param eUpgradePhase

A  <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_upgrade_phase">CLUSTER_UPGRADE_PHASE</a> enumeration values that indicates the state of the rolling upgrade.

## -returns

This function returns one of the following values:



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterupgradefunctionallevel">ClusterUpgradeFunctionalLevel</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Functions</a>