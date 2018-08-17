---
UID: NC:clusapi.PCLUSAPI_SET_CLUSTER_GROUP_NAME
title: PCLUSAPI_SET_CLUSTER_GROUP_NAME
author: windows-sdk-content
description: Sets the name for a group.
old-location: mscs\setclustergroupname.htm
old-project: mscs
ms.assetid: d2dc3837-24d3-4455-8e3e-bb74b95b1d44
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_GROUP_NAME, PCLUSAPI_SET_CLUSTER_GROUP_NAME callback, PCLUSAPI_SET_CLUSTER_GROUP_NAME callback function [Failover Cluster], _wolf_setclustergroupname, clusapi/PCLUSAPI_SET_CLUSTER_GROUP_NAME, mscs.setclustergroupname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_SET_CLUSTER_GROUP_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_SET_CLUSTER_GROUP_NAME callback function


## -description


Sets the name for a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>. The <b>PCLUSAPI_SET_CLUSTER_GROUP_NAME</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to name.


### -param lpszGroupName [in]

Pointer to the new name for the group identified by <i>hGroup</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



<i>SetClusterGroupName</i> changes the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> common property of the group identified by 
    <i>hGroup</i>. This is the only way that Name, a read-only property, can be changed.

Do not call <i>SetClusterGroupName</i> from a 
    resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

