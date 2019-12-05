---
UID: NF:clusapi.SetClusterGroupName
title: SetClusterGroupName function (clusapi.h)
description: Sets the name for a group.
old-location: mscs\setclustergroupname.htm
tech.root: MsCS
ms.assetid: d2dc3837-24d3-4455-8e3e-bb74b95b1d44
ms.date: 12/05/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_GROUP_NAME, PCLUSAPI_SET_CLUSTER_GROUP_NAME function [Failover Cluster], SetClusterGroupName, SetClusterGroupName function [Failover Cluster], _wolf_setclustergroupname, clusapi/PCLUSAPI_SET_CLUSTER_GROUP_NAME, clusapi/SetClusterGroupName, mscs.setclustergroupname
ms.topic: function
f1_keywords:
- clusapi/SetClusterGroupName
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ClusAPI.dll
- Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
- Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
- Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
- SetClusterGroupName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetClusterGroupName function


## -description


Sets the name for a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/groups">group</a>. The <b>PCLUSAPI_SET_CLUSTER_GROUP_NAME</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to name.


### -param lpszGroupName [in]

Pointer to the new name for the group identified by <i>hGroup</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.




## -remarks



<b>SetClusterGroupName</b> changes the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/groups-name">Name</a> common property of the group identified by 
    <i>hGroup</i>. This is the only way that Name, a read-only property, can be changed.

Do not call <b>SetClusterGroupName</b> from a 
    resource DLL. For more information, see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/groups-name">Name</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>
 

 

