---
UID: NF:resapi.ResUtilGetCoreClusterResourcesEx
title: ResUtilGetCoreClusterResourcesEx function (resapi.h)
description: Returns handles to the core,  Network Name, IP Address, and quorum resources. The PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX","PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX function [Failover Cluster]","ResUtilGetCoreClusterResourcesEx","ResUtilGetCoreClusterResourcesEx function [Failover Cluster]","mscs.resutilgetcoreclusterresourcesex","resapi/PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX","resapi/ResUtilGetCoreClusterResourcesEx"]
old-location: mscs\resutilgetcoreclusterresourcesex.htm
tech.root: MsCS
ms.assetid: F6C576C1-5D34-41EB-95A4-BC8F78F02414
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX, PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX function [Failover Cluster], ResUtilGetCoreClusterResourcesEx, ResUtilGetCoreClusterResourcesEx function [Failover Cluster], mscs.resutilgetcoreclusterresourcesex, resapi/PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX, resapi/ResUtilGetCoreClusterResourcesEx
req.header: resapi.h
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilGetCoreClusterResourcesEx
 - resapi/ResUtilGetCoreClusterResourcesEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
 - ext-ms-win-cluster-resutils-l1-1-0.dll
 - ext-ms-win-cluster-resutils-l1-1-1.dll
api_name:
 - ResUtilGetCoreClusterResourcesEx
---

# ResUtilGetCoreClusterResourcesEx function


## -description

Returns handles to the 
    <a href="/previous-versions/windows/desktop/mscs/core-resources">core</a>,  <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a>, 
    <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a>,  and 
    <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum</a> resources. The <b>PRESUTIL_GET_CORE_CLUSTER_RESOURCES_EX</b> type defines a pointer to this function.

## -parameters

### -param hClusterIn [in]

The cluster handle (see <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>).

### -param phClusterNameResourceOut [out]

A pointer to a resource handle to the core 
      <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resource for the 
      <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>, which stores the cluster name.

### -param phClusterQuorumResourceOut [out]

Not used.

### -param dwDesiredAccess [in]

The requested access privileges. This  might be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0), an undefined error  might be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetcoreclusterresources">ResUtilGetCoreClusterResources</a>.


#### - phClusterQuorumResource [out]

A pointer to a resource handle to the cluster's 
      <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a>.

## -returns

If the operations succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>