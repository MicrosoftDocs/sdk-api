---
UID: NF:clusapi.GetClusterFromNetwork
title: GetClusterFromNetwork function (clusapi.h)
description: Returns a handle to the cluster associated with a network.
helpviewer_keywords: ["GetClusterFromNetwork","GetClusterFromNetwork function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_FROM_NETWORK","PCLUSAPI_GET_CLUSTER_FROM_NETWORK function [Failover Cluster]","_wolf_getclusterfromnetwork","clusapi/GetClusterFromNetwork","clusapi/PCLUSAPI_GET_CLUSTER_FROM_NETWORK","mscs.getclusterfromnetwork"]
old-location: mscs\getclusterfromnetwork.htm
tech.root: MsCS
ms.assetid: 90ac313a-9f60-4591-b0fa-89d99b007280
ms.date: 12/05/2018
ms.keywords: GetClusterFromNetwork, GetClusterFromNetwork function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_NETWORK, PCLUSAPI_GET_CLUSTER_FROM_NETWORK function [Failover Cluster], _wolf_getclusterfromnetwork, clusapi/GetClusterFromNetwork, clusapi/PCLUSAPI_GET_CLUSTER_FROM_NETWORK, mscs.getclusterfromnetwork
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
 - GetClusterFromNetwork
 - clusapi/GetClusterFromNetwork
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
 - GetClusterFromNetwork
---

# GetClusterFromNetwork function


## -description

Returns a handle to the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> associated with a  <a href="/previous-versions/windows/desktop/mscs/networks">network</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_NETWORK</b> type defines a pointer to this function.

## -parameters

### -param hNetwork [in]

Handle to the network.

## -returns

If the operation succeeds, the function returns a handle to the cluster that owns the network.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For <i>hNetwork</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetwork">OpenClusterNetwork</a>).  <b>GetClusterFromNetwork</b> returns another instance of the handle from which <i>hNetwork</i> was obtained.

Be sure to call  <a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a> on the handle returned from  <b>GetClusterFromNetwork</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hNetwork</i> or the cluster handle from which <i>hNetwork</i> was obtained.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternetwork">CloseClusterNetwork</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromgroup">GetClusterFromGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnetinterface">GetClusterFromNetInterface</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnode">GetClusterFromNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromresource">GetClusterFromResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternetwork">OpenClusterNetwork</a>