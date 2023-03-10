---
UID: NF:clusapi.GetClusterFromResource
title: GetClusterFromResource function (clusapi.h)
description: Returns a handle to the cluster associated with a resource.
helpviewer_keywords: ["GetClusterFromResource","GetClusterFromResource function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_FROM_RESOURCE","PCLUSAPI_GET_CLUSTER_FROM_RESOURCE function [Failover Cluster]","_wolf_getclusterfromresource","clusapi/GetClusterFromResource","clusapi/PCLUSAPI_GET_CLUSTER_FROM_RESOURCE","mscs.getclusterfromresource"]
old-location: mscs\getclusterfromresource.htm
tech.root: MsCS
ms.assetid: d0ba93cb-94aa-4c68-b87e-518ee1e5c35c
ms.date: 12/05/2018
ms.keywords: GetClusterFromResource, GetClusterFromResource function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_RESOURCE, PCLUSAPI_GET_CLUSTER_FROM_RESOURCE function [Failover Cluster], _wolf_getclusterfromresource, clusapi/GetClusterFromResource, clusapi/PCLUSAPI_GET_CLUSTER_FROM_RESOURCE, mscs.getclusterfromresource
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
 - GetClusterFromResource
 - clusapi/GetClusterFromResource
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
 - GetClusterFromResource
---

# GetClusterFromResource function


## -description

Returns a handle to the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> associated with a  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the resource.

## -returns

If the operation succeeds, the function returns a handle to the cluster that owns the resource.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For <i>hResource</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>).  <b>GetClusterFromResource</b> returns another instance of the handle from which <i>hResource</i> was obtained.

Be sure to call  <a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a> on the handle returned from  <b>GetClusterFromResource</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hResource</i> or the cluster handle from which <i>hResource</i> was obtained.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromgroup">GetClusterFromGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnetinterface">GetClusterFromNetInterface</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnetwork">GetClusterFromNetwork</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnode">GetClusterFromNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>