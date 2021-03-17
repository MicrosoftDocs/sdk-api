---
UID: NF:clusapi.ClusterGetEnumCountEx
title: ClusterGetEnumCountEx function (clusapi.h)
description: Returns the number of cluster objects that are associated with a cluster enumeration handle.
helpviewer_keywords: ["ClusterGetEnumCountEx","ClusterGetEnumCountEx function [Failover Cluster]","PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX","PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX function [Failover Cluster]","clusapi/ClusterGetEnumCountEx","clusapi/PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX","mscs.clustergetenumcountex"]
old-location: mscs\clustergetenumcountex.htm
tech.root: MsCS
ms.assetid: EC66C1CF-4CAA-41C6-ABA1-BB576F0293F4
ms.date: 12/05/2018
ms.keywords: ClusterGetEnumCountEx, ClusterGetEnumCountEx function [Failover Cluster], PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX function [Failover Cluster], clusapi/ClusterGetEnumCountEx, clusapi/PCLUSAPI_CLUSTER_GET_ENUM_COUNT_EX, mscs.clustergetenumcountex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
 - ClusterGetEnumCountEx
 - clusapi/ClusterGetEnumCountEx
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
 - ClusterGetEnumCountEx
---

# ClusterGetEnumCountEx function


## -description

Returns the 
    number of cluster objects that are associated with a 
    cluster enumeration handle.

## -parameters

### -param hClusterEnum [in]

The handle to a cluster enumeration. This handle is obtained from the  
      <a href="/windows/desktop/api/clusapi/nf-clusapi-clusteropenenumex">ClusterOpenEnumEx</a>    function. A valid handle is required. This 
      parameter cannot be NULL.

## -returns

The number of 
       objects that are associated with the enumeration handle.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-management-functions">Failover Cluster Management Function</a>