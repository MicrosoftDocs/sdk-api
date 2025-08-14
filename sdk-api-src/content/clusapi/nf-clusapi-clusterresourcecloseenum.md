---
UID: NF:clusapi.ClusterResourceCloseEnum
title: ClusterResourceCloseEnum function (clusapi.h)
description: Closes a resource enumeration handle.
helpviewer_keywords: ["ClusterResourceCloseEnum","ClusterResourceCloseEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM","PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM function [Failover Cluster]","_wolf_clusterresourcecloseenum","clusapi/ClusterResourceCloseEnum","clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM","mscs.clusterresourcecloseenum"]
old-location: mscs\clusterresourcecloseenum.htm
tech.root: MsCS
ms.assetid: 49407b45-2b7f-43a2-90ff-98cc557edb31
ms.date: 12/05/2018
ms.keywords: ClusterResourceCloseEnum, ClusterResourceCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM function [Failover Cluster], _wolf_clusterresourcecloseenum, clusapi/ClusterResourceCloseEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM, mscs.clusterresourcecloseenum
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
 - ClusterResourceCloseEnum
 - clusapi/ClusterResourceCloseEnum
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - ClusterResourceCloseEnum
---

# ClusterResourceCloseEnum function


## -description

Closes a  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_CLOSE_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hResEnum [in]

A resource enumeration handle to be closed.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.
     If the operation fails, 
the function returns a different <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Cluster Resource Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceenum">ClusterResourceEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a>