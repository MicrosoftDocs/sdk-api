---
UID: NF:clusapi.ClusterCloseEnum
title: ClusterCloseEnum function (clusapi.h)
description: Closes a cluster enumeration handle originally opened by ClusterOpenEnum.
helpviewer_keywords: ["ClusterCloseEnum","ClusterCloseEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_CLOSE_ENUM","PCLUSAPI_CLUSTER_CLOSE_ENUM function [Failover Cluster]","_wolf_clustercloseenum","clusapi/ClusterCloseEnum","clusapi/PCLUSAPI_CLUSTER_CLOSE_ENUM","mscs.clustercloseenum"]
old-location: mscs\clustercloseenum.htm
tech.root: MsCS
ms.assetid: 3d7e45a0-d580-4d14-8795-2418bba40c73
ms.date: 12/05/2018
ms.keywords: ClusterCloseEnum, ClusterCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_CLOSE_ENUM, PCLUSAPI_CLUSTER_CLOSE_ENUM function [Failover Cluster], _wolf_clustercloseenum, clusapi/ClusterCloseEnum, clusapi/PCLUSAPI_CLUSTER_CLOSE_ENUM, mscs.clustercloseenum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - ClusterCloseEnum
 - clusapi/ClusterCloseEnum
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
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterCloseEnum
---

# ClusterCloseEnum function


## -description

Closes a cluster enumeration handle originally opened by  <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a>.

## -parameters

### -param hEnum [in]

Cluster enumeration handle to close. This is a handle originally returned by the  <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a> function.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterenum">ClusterEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a>