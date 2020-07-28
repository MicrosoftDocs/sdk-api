---
UID: NF:clusapi.ClusterGetEnumCount
title: ClusterGetEnumCount function (clusapi.h)
description: Returns the number of cluster objects associated with a cluster enumeration handle.
helpviewer_keywords: ["ClusterGetEnumCount","ClusterGetEnumCount function [Failover Cluster]","PCLUSAPI_CLUSTER_GET_ENUM_COUNT","PCLUSAPI_CLUSTER_GET_ENUM_COUNT function [Failover Cluster]","_wolf_clustergetenumcount","clusapi/ClusterGetEnumCount","clusapi/PCLUSAPI_CLUSTER_GET_ENUM_COUNT","mscs.clustergetenumcount"]
old-location: mscs\clustergetenumcount.htm
tech.root: MsCS
ms.assetid: 1f99a1d8-6d91-4114-b885-80775572ea7f
ms.date: 12/05/2018
ms.keywords: ClusterGetEnumCount, ClusterGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_GET_ENUM_COUNT function [Failover Cluster], _wolf_clustergetenumcount, clusapi/ClusterGetEnumCount, clusapi/PCLUSAPI_CLUSTER_GET_ENUM_COUNT, mscs.clustergetenumcount
f1_keywords:
- clusapi/ClusterGetEnumCount
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
- Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
- Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
- ClusterGetEnumCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterGetEnumCount function


## -description


Returns the 
    number of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> associated with a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_GET_ENUM_COUNT</b> type defines a pointer to this function.


## -parameters




### -param hEnum [in]

Handle to a cluster enumeration. This handle is obtained from 
      <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusteropenenum">ClusterOpenEnum</a>. A valid handle is required. This 
      parameter cannot be NULL.


## -returns



<b>ClusterGetEnumCount</b> returns the number of 
       objects associated with the enumeration handle.



