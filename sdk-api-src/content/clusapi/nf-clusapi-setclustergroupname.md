---
UID: NF:clusapi.SetClusterGroupName
title: SetClusterGroupName function (clusapi.h)
description: Sets the name for a group.
helpviewer_keywords: ["PCLUSAPI_SET_CLUSTER_GROUP_NAME","PCLUSAPI_SET_CLUSTER_GROUP_NAME function [Failover Cluster]","SetClusterGroupName","SetClusterGroupName function [Failover Cluster]","_wolf_setclustergroupname","clusapi/PCLUSAPI_SET_CLUSTER_GROUP_NAME","clusapi/SetClusterGroupName","mscs.setclustergroupname"]
old-location: mscs\setclustergroupname.htm
tech.root: MsCS
ms.assetid: d2dc3837-24d3-4455-8e3e-bb74b95b1d44
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_GROUP_NAME, PCLUSAPI_SET_CLUSTER_GROUP_NAME function [Failover Cluster], SetClusterGroupName, SetClusterGroupName function [Failover Cluster], _wolf_setclustergroupname, clusapi/PCLUSAPI_SET_CLUSTER_GROUP_NAME, clusapi/SetClusterGroupName, mscs.setclustergroupname
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
 - SetClusterGroupName
 - clusapi/SetClusterGroupName
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
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - SetClusterGroupName
---

# SetClusterGroupName function


## -description

Sets the name for a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a>. The <b>PCLUSAPI_SET_CLUSTER_GROUP_NAME</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

Handle to the group to name.

### -param lpszGroupName [in]

Pointer to the new name for the group identified by <i>hGroup</i>.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

<b>SetClusterGroupName</b> changes the 
    <a href="/previous-versions/windows/desktop/mscs/groups-name">Name</a> common property of the group identified by 
    <i>hGroup</i>. This is the only way that Name, a read-only property, can be changed.

Do not call <b>SetClusterGroupName</b> from a 
    resource DLL. For more information, see 
    <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/groups-name">Name</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>