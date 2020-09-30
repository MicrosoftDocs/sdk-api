---
UID: NF:clusapi.ClusterNetworkCloseEnum
title: ClusterNetworkCloseEnum function (clusapi.h)
description: Closes a network enumeration handle.
helpviewer_keywords: ["ClusterNetworkCloseEnum","ClusterNetworkCloseEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM","PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM function [Failover Cluster]","_wolf_clusternetworkcloseenum","clusapi/ClusterNetworkCloseEnum","clusapi/PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM","mscs.clusternetworkcloseenum"]
old-location: mscs\clusternetworkcloseenum.htm
tech.root: MsCS
ms.assetid: 725164c5-dc6d-42f4-a703-06336711e72e
ms.date: 12/05/2018
ms.keywords: ClusterNetworkCloseEnum, ClusterNetworkCloseEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM, PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM function [Failover Cluster], _wolf_clusternetworkcloseenum, clusapi/ClusterNetworkCloseEnum, clusapi/PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM, mscs.clusternetworkcloseenum
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
 - ClusterNetworkCloseEnum
 - clusapi/ClusterNetworkCloseEnum
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
 - ClusterNetworkCloseEnum
---

# ClusterNetworkCloseEnum function


## -description

Closes a  <a href="/previous-versions/windows/desktop/mscs/networks">network</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_NETWORK_CLOSE_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hNetworkEnum [in]

Handle to the network enumerator to close. This is a handle originally returned by the  <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkopenenum">ClusterNetworkOpenEnum</a> function.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkenum">ClusterNetworkEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkopenenum">ClusterNetworkOpenEnum</a>