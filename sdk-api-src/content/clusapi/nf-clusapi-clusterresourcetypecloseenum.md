---
UID: NF:clusapi.ClusterResourceTypeCloseEnum
title: ClusterResourceTypeCloseEnum function (clusapi.h)
description: Closes a resource type enumeration handle.
helpviewer_keywords: ["ClusterResourceTypeCloseEnum","ClusterResourceTypeCloseEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM","PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM function [Failover Cluster]","_wolf_clusterresourcetypecloseenum","clusapi/ClusterResourceTypeCloseEnum","clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM","mscs.clusterresourcetypecloseenum"]
old-location: mscs\clusterresourcetypecloseenum.htm
tech.root: MsCS
ms.assetid: c6524604-7a73-414c-95bb-dce9524f3295
ms.date: 12/05/2018
ms.keywords: ClusterResourceTypeCloseEnum, ClusterResourceTypeCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM, PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM function [Failover Cluster], _wolf_clusterresourcetypecloseenum, clusapi/ClusterResourceTypeCloseEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM, mscs.clusterresourcetypecloseenum
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
 - ClusterResourceTypeCloseEnum
 - clusapi/ClusterResourceTypeCloseEnum
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
 - ClusterResourceTypeCloseEnum
---

# ClusterResourceTypeCloseEnum function


## -description

Closes a <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_CLOSE_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hResTypeEnum [in]

Enumeration handle to be closed.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeenum">ClusterResourceTypeEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeopenenum">ClusterResourceTypeOpenEnum</a>