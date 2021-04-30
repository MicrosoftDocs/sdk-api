---
UID: NF:clusapi.ClusterNetworkOpenEnum
title: ClusterNetworkOpenEnum function (clusapi.h)
description: Opens an enumerator for iterating through objects on a network.
helpviewer_keywords: ["CLUSTER_NETWORK_ENUM_NETINTERFACES","ClusterNetworkOpenEnum","ClusterNetworkOpenEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM","PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM function [Failover Cluster]","_wolf_clusternetworkopenenum","clusapi/ClusterNetworkOpenEnum","clusapi/PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM","mscs.clusternetworkopenenum"]
old-location: mscs\clusternetworkopenenum.htm
tech.root: MsCS
ms.assetid: 59f6fd26-1d96-4b04-858d-bfd3e4d25d01
ms.date: 12/05/2018
ms.keywords: CLUSTER_NETWORK_ENUM_NETINTERFACES, ClusterNetworkOpenEnum, ClusterNetworkOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM, PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM function [Failover Cluster], _wolf_clusternetworkopenenum, clusapi/ClusterNetworkOpenEnum, clusapi/PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM, mscs.clusternetworkopenenum
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
 - ClusterNetworkOpenEnum
 - clusapi/ClusterNetworkOpenEnum
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
 - ClusterNetworkOpenEnum
---

# ClusterNetworkOpenEnum function


## -description

Opens an enumerator for iterating through <a href="/previous-versions/windows/desktop/mscs/cluster-objects">objects</a> on a 
    <a href="/previous-versions/windows/desktop/mscs/networks">network</a>. The <b>PCLUSAPI_CLUSTER_NETWORK_OPEN_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hNetwork [in]

A handle to a network.

### -param dwType [in]

A bitmask that describes the type of objects to be enumerated. One or more of the following values 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_network_enum">CLUSTER_NETWORK_ENUM</a> enumeration are valid.



#### CLUSTER_NETWORK_ENUM_NETINTERFACES (1)

Enumerates the network interface objects on the network.

## -returns

If the operation was successful, 
       <b>ClusterNetworkOpenEnum</b> returns a handle to a 
        network enumerator.

If the operation fails, the function returns <b>NULL</b>. For 
        more information about the error, call the function 
        <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Applications call the <b>ClusterNetworkOpenEnum</b> 
     function to create a particular type of enumerator. 
     <b>ClusterNetworkOpenEnum</b> can create enumerators 
     for iterating through all of the objects on a network or only the network interface objects. 
     <b>ClusterNetworkOpenEnum</b> returns a handle that 
     can be passed to <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkenum">ClusterNetworkEnum</a> to access each 
     of the objects to be enumerated and to 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkcloseenum">ClusterNetworkCloseEnum</a> to release the 
     enumerator.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/network-management-functions">Cluster Network Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkcloseenum">ClusterNetworkCloseEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusternetworkenum">ClusterNetworkEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetwork">OpenClusterNetwork</a>