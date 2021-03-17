---
UID: NF:clusapi.DeleteClusterGroupSet
title: DeleteClusterGroupSet function (clusapi.h)
description: Deletes the specified groupset from the cluster.
helpviewer_keywords: ["DeleteClusterGroupSet","DeleteClusterGroupSet function [Failover Cluster]","PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET","PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET function [Failover Cluster]","clusapi/DeleteClusterGroupSet","clusapi/PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET","mscs.deleteclustergroupcollection"]
old-location: mscs\deleteclustergroupcollection.htm
tech.root: MsCS
ms.assetid: 8787d61b-7a80-404c-985f-1ad4ba01acf0
ms.date: 12/05/2018
ms.keywords: DeleteClusterGroupSet, DeleteClusterGroupSet function [Failover Cluster], PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET, PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET function [Failover Cluster], clusapi/DeleteClusterGroupSet, clusapi/PCLUSAPI_DELETE_CLUSTER_GROUP_GROUPSET, mscs.deleteclustergroupcollection
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
 - DeleteClusterGroupSet
 - clusapi/DeleteClusterGroupSet
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
 - DeleteClusterGroupSet
---

# DeleteClusterGroupSet function


## -description

Deletes the specified groupset from the cluster. The groupset must contain no groups.

## -parameters

### -param hGroupSet [in]

A handle to the collection to be deleted

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.