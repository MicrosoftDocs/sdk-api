---
UID: NF:clusapi.ClusterGroupOpenEnum
title: ClusterGroupOpenEnum function (clusapi.h)
description: Opens an enumerator for iterating through a group's resources and/or the nodes that are included in its list of preferred owners.
helpviewer_keywords: ["CLUSTER_GROUP_ENUM_ALL","CLUSTER_GROUP_ENUM_CONTAINS","CLUSTER_GROUP_ENUM_NODES","ClusterGroupOpenEnum","ClusterGroupOpenEnum function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM","PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM function [Failover Cluster]","_wolf_clustergroupopenenum","clusapi/ClusterGroupOpenEnum","clusapi/PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM","mscs.clustergroupopenenum"]
old-location: mscs\clustergroupopenenum.htm
tech.root: MsCS
ms.assetid: d8f9eff0-1784-4b55-8603-c262d5c23f6c
ms.date: 12/05/2018
ms.keywords: CLUSTER_GROUP_ENUM_ALL, CLUSTER_GROUP_ENUM_CONTAINS, CLUSTER_GROUP_ENUM_NODES, ClusterGroupOpenEnum, ClusterGroupOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM, PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM function [Failover Cluster], _wolf_clustergroupopenenum, clusapi/ClusterGroupOpenEnum, clusapi/PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM, mscs.clustergroupopenenum
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
 - ClusterGroupOpenEnum
 - clusapi/ClusterGroupOpenEnum
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
 - ClusAPI.dll
api_name:
 - ClusterGroupOpenEnum
---

# ClusterGroupOpenEnum function


## -description

    Opens an enumerator for iterating through a 
    <a href="/previous-versions/windows/desktop/mscs/groups">group's</a> <a href="/previous-versions/windows/desktop/mscs/resources">resources</a> 
    and/or the <a href="/previous-versions/windows/desktop/mscs/nodes">nodes</a> that are included in its list of preferred 
    owners. The <b>PCLUSAPI_CLUSTER_GROUP_OPEN_ENUM</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

A handle to the <a href="/previous-versions/windows/desktop/mscs/groups">group</a> to be enumerated.

### -param dwType [in]

A bitmask that describes the <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> to be 
       enumerated. The following are valid values of the 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_group_enum">CLUSTER_GROUP_ENUM</a> enumeration.



#### CLUSTER_GROUP_ENUM_CONTAINS (1)

Enumerates the resources in the group.



#### CLUSTER_GROUP_ENUM_NODES (2)

Enumerates the nodes in the preferred owners list of the group.



#### CLUSTER_GROUP_ENUM_ALL (3)

Enumerates the resources in the group and the preferred owners of the group.

## -returns

If the operation succeeds, 
       <b>ClusterGroupOpenEnum</b> returns a handle to an 
       enumerator that can be passed to the 
       <a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupenum">ClusterGroupEnum</a> function.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the function <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Do not call <b>ClusterGroupOpenEnum</b> from any 
     resource DLL entry point function. 
     <b>ClusterGroupOpenEnum</b> can safely be called from a 
     worker thread. For more information, see 
     <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/enumerating-objects">Enumerating Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupcloseenum">ClusterGroupCloseEnum</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clustergroupenum">ClusterGroupEnum</a>



<a href="/previous-versions/windows/desktop/mscs/group-management-functions">Group Management Functions</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>