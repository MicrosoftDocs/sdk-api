---
UID: NF:clusapi.ClusterResourceTypeGetEnumCount
title: ClusterResourceTypeGetEnumCount function (clusapi.h)
description: Returns the number of cluster objects associated with a resource_type enumeration handle.
helpviewer_keywords: ["ClusterResourceTypeGetEnumCount","ClusterResourceTypeGetEnumCount function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT","PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT function [Failover Cluster]","_wolf_clusterresourcetypegetenumcount","clusapi/ClusterResourceTypeGetEnumCount","clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT","mscs.clusterresourcetypegetenumcount"]
old-location: mscs\clusterresourcetypegetenumcount.htm
tech.root: MsCS
ms.assetid: 1960dc1a-778e-4bad-b6ad-07c0a8547cc6
ms.date: 12/05/2018
ms.keywords: ClusterResourceTypeGetEnumCount, ClusterResourceTypeGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT function [Failover Cluster], _wolf_clusterresourcetypegetenumcount, clusapi/ClusterResourceTypeGetEnumCount, clusapi/PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT, mscs.clusterresourcetypegetenumcount
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
 - ClusterResourceTypeGetEnumCount
 - clusapi/ClusterResourceTypeGetEnumCount
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - ClusterResourceTypeGetEnumCount
---

# ClusterResourceTypeGetEnumCount function


## -description

Returns the number of  <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> associated with a  <a href="/previous-versions/windows/desktop/mscs/resource-types">resource_type</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_TYPE_GET_ENUM_COUNT</b> type defines a pointer to this function.

## -parameters

### -param hResTypeEnum [in]

Handle to a resource type enumeration. This handle is obtained from  <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypeopenenum">ClusterResourceTypeOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.

## -returns

<b>ClusterResourceTypeGetEnumCount</b> returns the number of objects associated with the enumeration handle.