---
UID: NF:clusapi.GetClusterFromGroupSet
title: GetClusterFromGroupSet function (clusapi.h)
description: GetClusterFromGroupSet function (clusapi.h) returns a handle to the cluster associated with a group set.
helpviewer_keywords: ["GetClusterFromGroupSet","GetClusterFromGroupSet function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_FROM_GROUP_GROUPSET","PCLUSAPI_GET_CLUSTER_FROM_GROUP_GROUPSET function [Failover Cluster]","clusapi/GetClusterFromGroupSet","clusapi/PCLUSAPI_GET_CLUSTER_FROM_GROUP_GROUPSET","mscs.getclusterfromgroupset"]
old-location: mscs\getclusterfromgroupset.htm
tech.root: MsCS
ms.assetid: 9d0669e3-8f4a-45f3-a2cc-c118bddcd791
ms.date: 08/03/2022
ms.keywords: GetClusterFromGroupSet, GetClusterFromGroupSet function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_GROUP_GROUPSET, PCLUSAPI_GET_CLUSTER_FROM_GROUP_GROUPSET function [Failover Cluster], clusapi/GetClusterFromGroupSet, clusapi/PCLUSAPI_GET_CLUSTER_FROM_GROUP_GROUPSET, mscs.getclusterfromgroupset
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - GetClusterFromGroupSet
 - clusapi/GetClusterFromGroupSet
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - GetClusterFromGroupSet
---

# GetClusterFromGroupSet function


## -description

Returns a handle to the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> associated with a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a> set. The <b>PCLUSAPI_GET_CLUSTER_FROM_GROUP_GROUPSET</b> type defines a pointer to this function.

## -parameters

### -param hGroupSet [in] [in]

A handle to the collection to be deleted

## -returns

If the operation succeeds, the function returns a handle to the cluster that owns the group.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
