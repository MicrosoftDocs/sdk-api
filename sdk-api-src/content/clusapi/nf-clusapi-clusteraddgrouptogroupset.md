---
UID: NF:clusapi.ClusterAddGroupToGroupSet
title: ClusterAddGroupToGroupSet function (clusapi.h)
description: Adds the specified group to a groupset in the cluster.
helpviewer_keywords: ["ClusterAddGroupToGroupSet","ClusterAddGroupToGroupSet function [Failover Cluster]","PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET","PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET function [Failover Cluster]","clusapi/ClusterAddGroupToGroupSet","clusapi/PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET","mscs.clusteraddgrouptogroupcollection"]
old-location: mscs\clusteraddgrouptogroupcollection.htm
tech.root: MsCS
ms.assetid: f201dfaa-d9e6-41e0-8d22-23c073b1789d
ms.date: 12/05/2018
ms.keywords: ClusterAddGroupToGroupSet, ClusterAddGroupToGroupSet function [Failover Cluster], PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET, PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET function [Failover Cluster], clusapi/ClusterAddGroupToGroupSet, clusapi/PCLUSAPI_CLUSTER_ADD_GROUP_TO_GROUP_GROUPSET, mscs.clusteraddgrouptogroupcollection
req.header: clusapi.h
req.include-header: 
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterAddGroupToGroupSet
 - clusapi/ClusterAddGroupToGroupSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterAddGroupToGroupSet
---

# ClusterAddGroupToGroupSet function


## -description

Adds the specified group to a groupset in the cluster. The group
    must not currently be in a groupset

## -parameters

### -param hGroupSet [in]

The collection to which to add the group

### -param hGroup [in]

The group to add to the collection

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.