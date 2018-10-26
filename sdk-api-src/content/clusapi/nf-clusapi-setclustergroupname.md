---
UID: NF:clusapi.SetClusterGroupName
title: SetClusterGroupName function
author: windows-sdk-content
description: Sets the name for a group.
old-location: mscs\setclustergroupname.htm
tech.root: mscs
ms.assetid: d2dc3837-24d3-4455-8e3e-bb74b95b1d44
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_GROUP_NAME, PCLUSAPI_SET_CLUSTER_GROUP_NAME function [Failover Cluster], SetClusterGroupName, SetClusterGroupName function [Failover Cluster], _wolf_setclustergroupname, clusapi/PCLUSAPI_SET_CLUSTER_GROUP_NAME, clusapi/SetClusterGroupName, mscs.setclustergroupname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClusterGroupName function


## -description


Sets the name for a  <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a>. The <b>PCLUSAPI_SET_CLUSTER_GROUP_NAME</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to name.


### -param lpszGroupName [in]

Pointer to the new name for the group identified by <i>hGroup</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<b>SetClusterGroupName</b> changes the 
    <a href="https://msdn.microsoft.com/2395438e-14d6-4a62-b3d9-c525bed8f652">Name</a> common property of the group identified by 
    <i>hGroup</i>. This is the only way that Name, a read-only property, can be changed.

Do not call <b>SetClusterGroupName</b> from a 
    resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/2395438e-14d6-4a62-b3d9-c525bed8f652">Name</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

