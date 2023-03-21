---
UID: NE:clusapi.CLUSTER_NODE_RESUME_FAILBACK_TYPE
title: CLUSTER_NODE_RESUME_FAILBACK_TYPE (clusapi.h)
description: Specifies the failback type to use when a cluster node in a paused state is resumed by the ResumeClusterNodeEx function.
helpviewer_keywords: ["CLUSTER_NODE_RESUME_FAILBACK_TYPE","CLUSTER_NODE_RESUME_FAILBACK_TYPE enumeration [Failover Cluster]","ClusterNodeResumeFailbackTypeCount","DoNotFailbackGroups","FailbackGroupsImmediately","FailbackGroupsPerPolicy","clusapi/CLUSTER_NODE_RESUME_FAILBACK_TYPE","clusapi/ClusterNodeResumeFailbackTypeCount","clusapi/DoNotFailbackGroups","clusapi/FailbackGroupsImmediately","clusapi/FailbackGroupsPerPolicy","mscs.cluster_node_resume_failback_type"]
old-location: mscs\cluster_node_resume_failback_type.htm
tech.root: MsCS
ms.assetid: 26A002F6-A933-450B-84FF-F2BC8B301B6B
ms.date: 12/05/2018
ms.keywords: CLUSTER_NODE_RESUME_FAILBACK_TYPE, CLUSTER_NODE_RESUME_FAILBACK_TYPE enumeration [Failover Cluster], ClusterNodeResumeFailbackTypeCount, DoNotFailbackGroups, FailbackGroupsImmediately, FailbackGroupsPerPolicy, clusapi/CLUSTER_NODE_RESUME_FAILBACK_TYPE, clusapi/ClusterNodeResumeFailbackTypeCount, clusapi/DoNotFailbackGroups, clusapi/FailbackGroupsImmediately, clusapi/FailbackGroupsPerPolicy, mscs.cluster_node_resume_failback_type
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CLUSTER_NODE_RESUME_FAILBACK_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_NODE_RESUME_FAILBACK_TYPE
 - clusapi/CLUSTER_NODE_RESUME_FAILBACK_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
api_name:
 - CLUSTER_NODE_RESUME_FAILBACK_TYPE
---

# CLUSTER_NODE_RESUME_FAILBACK_TYPE enumeration


## -description

Specifies the failback type to use when a cluster node in a paused state is resumed by the <a href="/windows/desktop/api/clusapi/nf-clusapi-resumeclusternodeex">ResumeClusterNodeEx</a> function.

## -enum-fields

### -field DoNotFailbackGroups:0

Indicates that the failback process is  not to  be performed on the specified groups.

### -field FailbackGroupsImmediately

Indicates that the groups is  to  be failed back to the node.

### -field FailbackGroupsPerPolicy

Indicates that the failover policy for each group is to  be used.

### -field ClusterNodeResumeFailbackTypeCount

Defines the maximum number of failback types.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-resumeclusternodeex">ResumeClusterNodeEx</a>
