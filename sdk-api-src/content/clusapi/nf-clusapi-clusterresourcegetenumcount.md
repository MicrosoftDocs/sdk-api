---
UID: NF:clusapi.ClusterResourceGetEnumCount
title: ClusterResourceGetEnumCount function (clusapi.h)
description: Returns the number of cluster objects associated with a resource enumeration handle.helpviewer_keywords: ["ClusterResourceGetEnumCount","ClusterResourceGetEnumCount function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT","PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT function [Failover Cluster]","_wolf_clusterresourcegetenumcount","clusapi/ClusterResourceGetEnumCount","clusapi/PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT","mscs.clusterresourcegetenumcount"]
old-location: mscs\clusterresourcegetenumcount.htm
tech.root: MsCS
ms.assetid: f837d57a-e7eb-4262-a1a3-e3bf9948cf09
ms.date: 12/05/2018
ms.keywords: ClusterResourceGetEnumCount, ClusterResourceGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT function [Failover Cluster], _wolf_clusterresourcegetenumcount, clusapi/ClusterResourceGetEnumCount, clusapi/PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT, mscs.clusterresourcegetenumcount
f1_keywords:
- clusapi/ClusterResourceGetEnumCount
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ClusAPI.dll
- Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
- ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
- ClusterResourceGetEnumCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterResourceGetEnumCount function


## -description


Returns the number of  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> associated with a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resources">resource</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hResEnum [in]

Handle to a resource enumeration. This handle is obtained from  <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenum">ClusterResourceOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



<b>ClusterResourceGetEnumCount</b> returns the number of objects associated with the enumeration handle.



