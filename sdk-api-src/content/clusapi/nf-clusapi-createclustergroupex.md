---
UID: NF:clusapi.CreateClusterGroupEx
title: CreateClusterGroupEx function (clusapi.h)
description: Creates a new cluster group with the options specified in the CLUSTER_CREATE_GROUP_INFO structure in a single operation.
helpviewer_keywords: ["CreateClusterGroupEx","CreateClusterGroupEx function [Failover Cluster]","PCLUSAPI_CREATE_CLUSTER_GROUPEX","PCLUSAPI_CREATE_CLUSTER_GROUPEX function [Failover Cluster]","clusapi/CreateClusterGroupEx","clusapi/PCLUSAPI_CREATE_CLUSTER_GROUPEX","mscs.createclustergroupex"]
old-location: mscs\createclustergroupex.htm
tech.root: MsCS
ms.assetid: D24A2622-758D-4344-8872-F0D8E4EE80CC
ms.date: 12/05/2018
ms.keywords: CreateClusterGroupEx, CreateClusterGroupEx function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_GROUPEX, PCLUSAPI_CREATE_CLUSTER_GROUPEX function [Failover Cluster], clusapi/CreateClusterGroupEx, clusapi/PCLUSAPI_CREATE_CLUSTER_GROUPEX, mscs.createclustergroupex
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateClusterGroupEx
 - clusapi/CreateClusterGroupEx
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
 - ext-ms-win-cluster-clusapi-l1-1-2.dll
api_name:
 - CreateClusterGroupEx
---

# CreateClusterGroupEx function


## -description

Creates a new cluster group with the options specified in the <b>CLUSTER_CREATE_GROUP_INFO</b> structure in a single operation.The <b>PCLUSAPI_CREATE_CLUSTER_GROUPEX</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

The handle to the cluster in which the group will be created.

### -param lpszGroupName [in]

The name of the new cluster group.

### -param pGroupInfo [in, optional]

The additional information used to create the group.

## -returns

If the operation is successful, the function returns a handle to the newly created group.
If the operation fails, the function returns <b>NULL</b>.

## -remarks

The <b>CLUSTER_CREATE_GROUP_INFO</b> structure enables additional properties for group creation.  Currently, only the group type can be specified, which  enables the group type to be set when the group is created.

