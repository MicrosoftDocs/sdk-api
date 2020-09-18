---
UID: NF:clusapi.CreateClusterGroupSet
title: CreateClusterGroupSet function (clusapi.h)
description: Adds a groupset to a cluster and returns a handle to the newly added groupset.
helpviewer_keywords: ["CreateClusterGroupSet","CreateClusterGroupSet function [Failover Cluster]","PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET","PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET function [Failover Cluster]","clusapi/CreateClusterGroupSet","clusapi/PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET","mscs.createclustergroupcollection"]
old-location: mscs\createclustergroupcollection.htm
tech.root: MsCS
ms.assetid: cb0cdf78-c6d6-47b3-bd11-5ab70416131b
ms.date: 12/05/2018
ms.keywords: CreateClusterGroupSet, CreateClusterGroupSet function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET, PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET function [Failover Cluster], clusapi/CreateClusterGroupSet, clusapi/PCLUSAPI_CREATE_CLUSTER_GROUP_GROUPSET, mscs.createclustergroupcollection
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
 - CreateClusterGroupSet
 - clusapi/CreateClusterGroupSet
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
 - CreateClusterGroupSet
---

# CreateClusterGroupSet function


## -description

Adds a  groupset to a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to the newly added groupset.

## -parameters

### -param hCluster [in]

A handle to the target cluster.

### -param groupSetName [in]

Pointer to a null-terminated Unicode string containing the name of the groupset to be added.

## -returns

If the operation succeeds, 
returns a groupset handle.

If the operation fails, 
returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.