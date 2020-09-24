---
UID: NF:clusapi.GetClusterFromNode
title: GetClusterFromNode function (clusapi.h)
description: Returns a handle to the cluster associated with a node.
helpviewer_keywords: ["GetClusterFromNode","GetClusterFromNode function [Failover Cluster]","PCLUSAPI_GET_CLUSTER_FROM_NODE","PCLUSAPI_GET_CLUSTER_FROM_NODE function [Failover Cluster]","_wolf_getclusterfromnode","clusapi/GetClusterFromNode","clusapi/PCLUSAPI_GET_CLUSTER_FROM_NODE","mscs.getclusterfromnode"]
old-location: mscs\getclusterfromnode.htm
tech.root: MsCS
ms.assetid: 8cc0f881-fbf2-452c-a044-58939f4e01ea
ms.date: 12/05/2018
ms.keywords: GetClusterFromNode, GetClusterFromNode function [Failover Cluster], PCLUSAPI_GET_CLUSTER_FROM_NODE, PCLUSAPI_GET_CLUSTER_FROM_NODE function [Failover Cluster], _wolf_getclusterfromnode, clusapi/GetClusterFromNode, clusapi/PCLUSAPI_GET_CLUSTER_FROM_NODE, mscs.getclusterfromnode
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
 - GetClusterFromNode
 - clusapi/GetClusterFromNode
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
 - GetClusterFromNode
---

# GetClusterFromNode function


## -description

Returns a handle to the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> associated with a  <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>. The <b>PCLUSAPI_GET_CLUSTER_FROM_NODE</b> type defines a pointer to this function.

## -parameters

### -param hNode [in]

Handle to the node.

## -returns

If the operation succeeds, the function returns a handle to the cluster that owns the node.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For <i>hNode</i> to be a valid handle, there must necessarily be an open cluster handle (see  <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>).  <b>GetClusterFromNode</b> returns another instance of the handle from which <i>hNode</i> was obtained.

Be sure to call  <a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a> on the handle returned from  <b>GetClusterFromNode</b> before the handle goes out of scope. Closing this handle does not invalidate <i>hNode</i> or the cluster handle from which <i>hNode</i> was obtained.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closecluster">CloseCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusternode">CloseClusterNode</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromgroup">GetClusterFromGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnetinterface">GetClusterFromNetInterface</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromnetwork">GetClusterFromNetwork</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-getclusterfromresource">GetClusterFromResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>