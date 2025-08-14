---
UID: NF:clusapi.CreateClusterGroup
title: CreateClusterGroup function (clusapi.h)
description: Adds a group to a cluster and returns a handle to the newly added group.
helpviewer_keywords: ["CreateClusterGroup","CreateClusterGroup function [Failover Cluster]","PCLUSAPI_CREATE_CLUSTER_GROUP","PCLUSAPI_CREATE_CLUSTER_GROUP function [Failover Cluster]","_wolf_createclustergroup","clusapi/CreateClusterGroup","clusapi/PCLUSAPI_CREATE_CLUSTER_GROUP","mscs.createclustergroup"]
old-location: mscs\createclustergroup.htm
tech.root: MsCS
ms.assetid: 7011640e-87d0-4f2b-971c-9e86c77db13e
ms.date: 12/05/2018
ms.keywords: CreateClusterGroup, CreateClusterGroup function [Failover Cluster], PCLUSAPI_CREATE_CLUSTER_GROUP, PCLUSAPI_CREATE_CLUSTER_GROUP function [Failover Cluster], _wolf_createclustergroup, clusapi/CreateClusterGroup, clusapi/PCLUSAPI_CREATE_CLUSTER_GROUP, mscs.createclustergroup
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
 - CreateClusterGroup
 - clusapi/CreateClusterGroup
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
 - CreateClusterGroup
---

# CreateClusterGroup function


## -description

Adds a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a> to a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to the newly added group. The <b>PCLUSAPI_CREATE_CLUSTER_GROUP</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to the target cluster.

### -param lpszGroupName [in]

Pointer to a null-terminated Unicode string containing the name of the group to be added to the cluster identified by <i>hCluster</i>. If there is not a group by this name,  <b>CreateClusterGroup</b> creates it.

## -returns

If the operation succeeds, 
the function returns a group handle.

If the operation fails, 
the function returns <b>NULL</b>. For more information about the error, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not call  <b>CreateClusterGroup</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

The <b>CreateClusterGroup</b> function calls the <a href="/windows/desktop/api/clusapi/nf-clusapi-createclustergroupex">CreateClusterGroupEx</a> function with a <b>NULL</b> CLUSTER_CREATE_GROUP_INFO. The new group is created with a group type of ClusGroupTypeUnknown.


#### Examples

See  <a href="/previous-versions/windows/desktop/mscs/creating-groups">Creating Groups</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>