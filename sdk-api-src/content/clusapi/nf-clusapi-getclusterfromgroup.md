---
UID: NF:clusapi.GetClusterFromGroup
title: GetClusterFromGroup function (clusapi.h)
description: Returns a handle to the cluster associated with a group.
helpviewer_keywords: ["GetClusterFromGroup","GetClusterFromGroup function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_FROM_GROUP","PCLUSAPI_GET_CLUSTER_FROM_GROUP function [Failover Cluster]","_wolf_getclusterfromgroup","clusapi/GetClusterFromGroup","clusapi/PCLUSAPI_GET_CLUSTER_FROM_GROUP","mscs.getclusterfromgroup"]
old-location: mscs\getclusterfromgroup.htm
tech.root: MsCS
ms.assetid: 43e1a74f-3320-4b1a-a946-6485d380dda1
ms.date: 12/05/2018
ms.keywords: GetClusterFromGroup, GetClusterFromGroup function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_GROUP, PCLUSAPI_GET_CLUSTER_FROM_GROUP function [Failover Cluster], _wolf_getclusterfromgroup, clusapi/GetClusterFromGroup, clusapi/PCLUSAPI_GET_CLUSTER_FROM_GROUP, mscs.getclusterfromgroup
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
 - GetClusterFromGroup
 - clusapi/GetClusterFromGroup
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
 - GetClusterFromGroup
---

# GetClusterFromGroup function


## -description

Returns a handle to the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> associated with a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_GROUP</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

Handle to the group.

## -returns

If the operation succeeds, the function returns a handle to the cluster that owns the group.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For <i>hGroup</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>).  <b>GetClusterFromGroup</b> returns another instance of the handle from which <i>hGroup</i> was obtained.

Be sure to call  <a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a> on the handle returned from  <b>GetClusterFromGroup</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hGroup</i> or the cluster handle from which <i>hGroup</i> was obtained.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnetinterface">GetClusterFromNetInterface</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnetwork">GetClusterFromNetwork</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnode">GetClusterFromNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromresource">GetClusterFromResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>