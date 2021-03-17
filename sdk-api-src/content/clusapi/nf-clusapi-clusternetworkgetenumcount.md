---
UID: NF:clusapi.ClusterNetworkGetEnumCount
title: ClusterNetworkGetEnumCount function (clusapi.h)
description: Returns the number of cluster objects associated with a network enumeration handle.
helpviewer_keywords: ["ClusterNetworkGetEnumCount","ClusterNetworkGetEnumCount function [Failover Cluster]","PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT","PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT function [Failover Cluster]","_wolf_clusternetworkgetenumcount","clusapi/ClusterNetworkGetEnumCount","clusapi/PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT","mscs.clusternetworkgetenumcount"]
old-location: mscs\clusternetworkgetenumcount.htm
tech.root: MsCS
ms.assetid: b3397d85-4e9a-4ee8-ba81-25185e2d46fd
ms.date: 12/05/2018
ms.keywords: ClusterNetworkGetEnumCount, ClusterNetworkGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT function [Failover Cluster], _wolf_clusternetworkgetenumcount, clusapi/ClusterNetworkGetEnumCount, clusapi/PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT, mscs.clusternetworkgetenumcount
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
 - ClusterNetworkGetEnumCount
 - clusapi/ClusterNetworkGetEnumCount
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
 - ClusterNetworkGetEnumCount
---

# ClusterNetworkGetEnumCount function


## -description

Returns the number of <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> associated with a 
    <a href="/previous-versions/windows/desktop/mscs/networks">network</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_NETWORK_GET_ENUM_COUNT</b> type defines a pointer to this function.

## -parameters

### -param hNetworkEnum [in]

Handle to a network enumeration. This handle is obtained from 
      <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkopenenum">ClusterNetworkOpenEnum</a>. A valid handle is 
      required. This parameter cannot be <b>NULL</b>.

## -returns

<b>ClusterNetworkGetEnumCount</b> returns the 
       number of objects associated with the enumeration handle.