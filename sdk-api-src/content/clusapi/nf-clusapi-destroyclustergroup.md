---
UID: NF:clusapi.DestroyClusterGroup
title: DestroyClusterGroup function (clusapi.h)
description: Deletes the specified group from a cluster.
helpviewer_keywords: ["DestroyClusterGroup","DestroyClusterGroup function [Failover Cluster]","PCLUSAPI_DESTROY_CLUSTER_GROUP","PCLUSAPI_DESTROY_CLUSTER_GROUP function [Failover Cluster]","clusapi/DestroyClusterGroup","clusapi/PCLUSAPI_DESTROY_CLUSTER_GROUP","mscs.destroyclustergroup"]
old-location: mscs\destroyclustergroup.htm
tech.root: MsCS
ms.assetid: ac293d5b-edc8-4c5f-9b05-9e2349bf1453
ms.date: 12/05/2018
ms.keywords: DestroyClusterGroup, DestroyClusterGroup function [Failover Cluster], PCLUSAPI_DESTROY_CLUSTER_GROUP, PCLUSAPI_DESTROY_CLUSTER_GROUP function [Failover Cluster], clusapi/DestroyClusterGroup, clusapi/PCLUSAPI_DESTROY_CLUSTER_GROUP, mscs.destroyclustergroup
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
 - DestroyClusterGroup
 - clusapi/DestroyClusterGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - DestroyClusterGroup
---

# DestroyClusterGroup function


## -description

Deletes the specified <a href="/previous-versions/windows/desktop/mscs/groups">group</a> from a 
    <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>. Unlike 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-deleteclustergroup">DeleteClusterGroup</a> the group can contain resources 
    and it can be online. The <b>PCLUSAPI_DESTROY_CLUSTER_GROUP</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

This parameter takes a handle to the cluster group to be destroyed.

## -returns

This function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. If the 
       operation completes successfully the function returns <b>ERROR_SUCCESS</b> (0). Any other 
       returned system error code would indicate that the 
       operation failed.

## -remarks

The <b>PCLUSAPI_DESTROY_CLUSTER_GROUP</b> type defines a pointer to this function.

<b>DestroyClusterGroup</b> does not close the group 
     handle specified by the <i>hGroup</i> parameter. To avoid memory leaks, be sure to close this handle with 
     the <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclustergroup">CloseClusterGroup</a> function.

Do not call <b>DestroyClusterGroup</b> from a resource 
     DLL. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclustergroup">CloseClusterGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-deleteclustergroup">DeleteClusterGroup</a>



<a href="/previous-versions/windows/desktop/mscs/group-management-functions">Group Management Functions</a>