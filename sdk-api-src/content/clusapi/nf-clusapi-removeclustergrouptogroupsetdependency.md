---
UID: NF:clusapi.RemoveClusterGroupToGroupSetDependency
title: RemoveClusterGroupToGroupSetDependency function (clusapi.h)
description: Removes a groupset from a group's dependency expression.
helpviewer_keywords: ["PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY","PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster]","RemoveClusterGroupToGroupSetDependency","RemoveClusterGroupToGroupSetDependency function [Failover Cluster]","clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY","clusapi/RemoveClusterGroupToGroupSetDependency","mscs.removeclustergrouptogroupcollectiondependency"]
old-location: mscs\removeclustergrouptogroupcollectiondependency.htm
tech.root: MsCS
ms.assetid: 2bd7e1f4-0b88-466f-a408-dddb9a11a52d
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY function [Failover Cluster], RemoveClusterGroupToGroupSetDependency, RemoveClusterGroupToGroupSetDependency function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_TO_GROUP_GROUPSET_DEPENDENCY, clusapi/RemoveClusterGroupToGroupSetDependency, mscs.removeclustergrouptogroupcollectiondependency
f1_keywords:
- clusapi/RemoveClusterGroupToGroupSetDependency
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ClusAPI.dll
api_name:
- RemoveClusterGroupToGroupSetDependency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemoveClusterGroupToGroupSetDependency function


## -description


Removes a groupset from a group's dependency expression.


## -parameters




### -param hGroup [in]

The group from which to remove the dependency.


### -param hDependsOn [in]

The groupset to remove.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.



