---
UID: NF:clusapi.RemoveClusterGroupSetDependency
title: RemoveClusterGroupSetDependency function (clusapi.h)
description: Removes a groupset from a groupset's dependency expression.
helpviewer_keywords: ["PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY","PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster]","RemoveClusterGroupSetDependency","RemoveClusterGroupSetDependency function [Failover Cluster]","clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY","clusapi/RemoveClusterGroupSetDependency","mscs.removeclustergroupcollectiondependency"]
old-location: mscs\removeclustergroupcollectiondependency.htm
tech.root: MsCS
ms.assetid: 1a9dcc3f-e73a-4f14-a418-b1c62a0c98c2
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster], RemoveClusterGroupSetDependency, RemoveClusterGroupSetDependency function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_GROUPSET_DEPENDENCY, clusapi/RemoveClusterGroupSetDependency, mscs.removeclustergroupcollectiondependency
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
 - RemoveClusterGroupSetDependency
 - clusapi/RemoveClusterGroupSetDependency
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
 - RemoveClusterGroupSetDependency
---

# RemoveClusterGroupSetDependency function


## -description

Removes a groupset from a groupset's dependency expression.

## -parameters

### -param hGroupSet [in]

The groupset from which to remove the dependency.

### -param hDependsOn [in]

The collection to remove

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.