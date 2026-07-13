---
UID: NF:clusapi.ClusterGroupOpenEnumEx
title: ClusterGroupOpenEnumEx function (clusapi.h)
description: Opens a handle to the group enumeration.
helpviewer_keywords: ["ClusterGroupOpenEnumEx","ClusterGroupOpenEnumEx function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX","PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX function [Failover Cluster]","clusapi/ClusterGroupOpenEnumEx","clusapi/PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX","mscs.clustergroupopenenumex"]
old-location: mscs\clustergroupopenenumex.htm
tech.root: MsCS
ms.assetid: 1BEF74A2-8230-4698-A3B7-FC2AA495D294
ms.date: 12/05/2018
ms.keywords: ClusterGroupOpenEnumEx, ClusterGroupOpenEnumEx function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX, PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX function [Failover Cluster], clusapi/ClusterGroupOpenEnumEx, clusapi/PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX, mscs.clustergroupopenenumex
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
 - ClusterGroupOpenEnumEx
 - clusapi/ClusterGroupOpenEnumEx
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterGroupOpenEnumEx
---

# ClusterGroupOpenEnumEx function


## -description

Opens a handle to the group enumeration.The <b>PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM_EX</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

The handle to the cluster on which the enumeration will be performed.

### -param lpszProperties

A pointer to a list of names of common properties.

### -param cbProperties [in]

The size, in bytes, of the <b>lpszProperties</b> field.

### -param lpszRoProperties

A pointer to a list of names of read-only common properties.

### -param cbRoProperties [in]

The size, in bytes, of the <b>lpszRoProperties</b> field.

### -param dwFlags [in]

Reserved for future use. This value must be 0.

## -returns

If the operation is successful, the function returns a handle to the enumeration.

If the operation fails, the function returns <b>NULL</b>.

## -remarks

The <b>ClusterGroupOpenEnumEx</b> function connects to the cluster service via remote procedure call (RPC) and gathers all of the data to handle the entire enumeration.  After the RPC call completes, the data is maintained locally.  The <b>HGROUPENUMEX</b> handle contains all of the data required to satisfy the enumeration.  Additional calls to <a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupenumex">ClusterGroupEnumEx</a>   or <a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupgetenumcountex">ClusterGroupGetEnumCountEx</a> do not connect to the cluster.