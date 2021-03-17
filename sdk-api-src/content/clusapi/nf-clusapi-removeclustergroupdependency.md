---
UID: NF:clusapi.RemoveClusterGroupDependency
title: RemoveClusterGroupDependency function (clusapi.h)
description: Removes a dependency between two cluster groups.
helpviewer_keywords: ["PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY","PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY function [Failover Cluster]","RemoveClusterGroupDependency","RemoveClusterGroupDependency function [Failover Cluster]","clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY","clusapi/RemoveClusterGroupDependency","mscs.removeclustergroupdependency"]
old-location: mscs\removeclustergroupdependency.htm
tech.root: MsCS
ms.assetid: da264d42-28ee-4589-a790-51da9f788ee9
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY function [Failover Cluster], RemoveClusterGroupDependency, RemoveClusterGroupDependency function [Failover Cluster], clusapi/PCLUSAPI_REMOVE_CLUSTER_GROUP_DEPENDENCY, clusapi/RemoveClusterGroupDependency, mscs.removeclustergroupdependency
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
 - RemoveClusterGroupDependency
 - clusapi/RemoveClusterGroupDependency
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
 - RemoveClusterGroupDependency
---

# RemoveClusterGroupDependency function


## -description

Removes a dependency between two cluster groups.

## -parameters

### -param hGroup [in]

The dependent group

### -param hDependsOn [in]

The group <i>hDependentGroup</i> depends on

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.