---
UID: NF:clusapi.DeleteClusterGroup
title: DeleteClusterGroup function (clusapi.h)
description: Removes an offline and empty group from a cluster.
helpviewer_keywords: ["DeleteClusterGroup","DeleteClusterGroup function [Failover Cluster]","PCLUSAPI_DELETE_CLUSTER_GROUP","PCLUSAPI_DELETE_CLUSTER_GROUP function [Failover Cluster]","_wolf_deleteclustergroup","clusapi/DeleteClusterGroup","clusapi/PCLUSAPI_DELETE_CLUSTER_GROUP","mscs.deleteclustergroup"]
old-location: mscs\deleteclustergroup.htm
tech.root: MsCS
ms.assetid: a0a8461c-8919-4620-83a2-bb8e5d03b0c4
ms.date: 12/05/2018
ms.keywords: DeleteClusterGroup, DeleteClusterGroup function [Failover Cluster], PCLUSAPI_DELETE_CLUSTER_GROUP, PCLUSAPI_DELETE_CLUSTER_GROUP function [Failover Cluster], _wolf_deleteclustergroup, clusapi/DeleteClusterGroup, clusapi/PCLUSAPI_DELETE_CLUSTER_GROUP, mscs.deleteclustergroup
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
 - DeleteClusterGroup
 - clusapi/DeleteClusterGroup
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
 - DeleteClusterGroup
---

# DeleteClusterGroup function


## -description

Removes an offline and empty 
    <a href="/previous-versions/windows/desktop/mscs/groups">group</a> from a 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_GROUP</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

Handle to the group to be removed. You must close this handle separately.

## -returns

This function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. If the 
       operation completes successfully the function returns <b>ERROR_SUCCESS</b> (0). Any other 
       returned system error code would indicate that the 
       operation failed.

## -remarks

The <b>PCLUSAPI_DELETE_CLUSTER_GROUP</b> type defines a pointer to this function.

Because the <b>DeleteClusterGroup</b> function only 
     removes groups that are empty, a group must not have any 
     <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> if it is to be successfully deleted. To delete a group 
     with resources, use the <a href="/windows/desktop/api/clusapi/nf-clusapi-destroyclustergroup">DestroyClusterGroup</a> 
     function.

<b>DeleteClusterGroup</b> does not close the group 
     handle specified by <i>hGroup</i>. To avoid memory leaks, be sure to close this handle with 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclustergroup">CloseClusterGroup</a>.

Do not call <b>DeleteClusterGroup</b> from a resource 
     DLL. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclustergroup">CloseClusterGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-createclustergroup">CreateClusterGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-destroyclustergroup">DestroyClusterGroup</a>



<a href="/previous-versions/windows/desktop/mscs/group-management-functions">Group Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>