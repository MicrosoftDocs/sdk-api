---
UID: NF:clusapi.ClusterResourceGetEnumCountEx
title: ClusterResourceGetEnumCountEx function (clusapi.h)
description: Returns the number of cluster objects that are associated with a resource enumeration handle.
helpviewer_keywords: ["ClusterResourceGetEnumCountEx","ClusterResourceGetEnumCountEx function [Failover Cluster]","PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX","PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX function [Failover Cluster]","clusapi/ClusterResourceGetEnumCountEx","clusapi/PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX","mscs.clusterresourcegetenumcountex"]
old-location: mscs\clusterresourcegetenumcountex.htm
tech.root: MsCS
ms.assetid: 97C22642-F968-4E41-90BC-28DF8DF5886C
ms.date: 12/05/2018
ms.keywords: ClusterResourceGetEnumCountEx, ClusterResourceGetEnumCountEx function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX, PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX function [Failover Cluster], clusapi/ClusterResourceGetEnumCountEx, clusapi/PCLUSAPI_CLUSTER_RESOURCE_GET_ENUM_COUNT_EX, mscs.clusterresourcegetenumcountex
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
 - ClusterResourceGetEnumCountEx
 - clusapi/ClusterResourceGetEnumCountEx
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
 - ClusterResourceGetEnumCountEx
---

# ClusterResourceGetEnumCountEx function


## -description

Returns the number of  <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a>  that are associated with a  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> enumeration handle.

## -parameters

### -param hResourceEnumEx [in]

The handle to a resource enumeration. This handle is obtained from 
the <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenumex">ClusterResourceOpenEnumEx</a> function. A valid handle is required. This parameter cannot be <b>NULL</b>.

## -returns

The number of objects that are associated with the enumeration handle.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterresourceopenenumex">ClusterResourceOpenEnumEx</a>



<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>