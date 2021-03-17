---
UID: NF:clusapi.GetClusterResourceNetworkName
title: GetClusterResourceNetworkName function (clusapi.h)
description: Retrieves the Name private property of the Network Name resource on which a resource is dependent.
helpviewer_keywords: ["GetClusterResourceNetworkName","GetClusterResourceNetworkName function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME","PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME function [Failover Cluster]","_wolf_getclusterresourcenetworkname","clusapi/GetClusterResourceNetworkName","clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME","mscs.getclusterresourcenetworkname"]
old-location: mscs\getclusterresourcenetworkname.htm
tech.root: MsCS
ms.assetid: db3cdaa6-d686-48be-be4a-468910813d6d
ms.date: 12/05/2018
ms.keywords: GetClusterResourceNetworkName, GetClusterResourceNetworkName function [Failover Cluster], PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME, PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME function [Failover Cluster], _wolf_getclusterresourcenetworkname, clusapi/GetClusterResourceNetworkName, clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME, mscs.getclusterresourcenetworkname
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
 - GetClusterResourceNetworkName
 - clusapi/GetClusterResourceNetworkName
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
 - GetClusterResourceNetworkName
---

# GetClusterResourceNetworkName function


## -description

Retrieves the <a href="/previous-versions/windows/desktop/mscs/network-names-name">Name</a> private property of the 
    <a href="/previous-versions/windows/desktop/mscs/network-name">Network Name</a> resource on 
    which a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> is 
    <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependent</a>. The <b>PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the dependent resource.

### -param lpBuffer [out]

Buffer containing a null-terminated Unicode string that contains the 
      <a href="/previous-versions/windows/desktop/mscs/network-names-name">Name</a> private property of the Network Name 
      resource on which the resource depends.

### -param nSize [in, out]

On input, pointer to a count of characters in the buffer pointed to by <i>lpBuffer</i>. 
      On output, pointer to a count of characters in the network name of the Network Name resource contained in the 
      buffer pointed to by <i>lpBuffer</i>, excluding the null-terminating character.

## -returns

If the operation succeeds, the function returns <b>TRUE</b>.

If the operation fails, the function returns <b>FALSE</b>. For more information about the 
       error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not call 
    <b>GetClusterResourceNetworkName</b> from any 
    resource DLL entry point function. 
    <b>GetClusterResourceNetworkName</b> can safely 
    be called from a worker thread. For more information, see 
    <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Cluster Resource Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>