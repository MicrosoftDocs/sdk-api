---
UID: NF:clusapi.DeleteClusterGroup
title: DeleteClusterGroup function
author: windows-sdk-content
description: Removes an offline and empty group from a cluster.
old-location: mscs\deleteclustergroup.htm
tech.root: MsCS
ms.assetid: a0a8461c-8919-4620-83a2-bb8e5d03b0c4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DeleteClusterGroup, DeleteClusterGroup function [Failover Cluster], PCLUSAPI_DELETE_CLUSTER_GROUP, PCLUSAPI_DELETE_CLUSTER_GROUP function [Failover Cluster], _wolf_deleteclustergroup, clusapi/DeleteClusterGroup, clusapi/PCLUSAPI_DELETE_CLUSTER_GROUP, mscs.deleteclustergroup
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
api_name:
 - DeleteClusterGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DeleteClusterGroup
: 
---

# DeleteClusterGroup function


## -description


Removes an offline and empty 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> from a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to be removed. You must close this handle separately.


## -returns



This function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>. If the 
       operation completes successfully the function returns <b>ERROR_SUCCESS</b> (0). Any other 
       returned system error code would indicate that the 
       operation failed.




## -remarks



The <b>PCLUSAPI_DELETE_CLUSTER_GROUP</b> type defines a pointer to this function.

Because the <b>DeleteClusterGroup</b> function only 
     removes groups that are empty, a group must not have any 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a> if it is to be successfully deleted. To delete a group 
     with resources, use the <a href="https://msdn.microsoft.com/ac293d5b-edc8-4c5f-9b05-9e2349bf1453">DestroyClusterGroup</a> 
     function.

<b>DeleteClusterGroup</b> does not close the group 
     handle specified by <i>hGroup</i>. To avoid memory leaks, be sure to close this handle with 
     <a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>.

Do not call <b>DeleteClusterGroup</b> from a resource 
     DLL. For more information, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>



<a href="https://msdn.microsoft.com/7011640e-87d0-4f2b-971c-9e86c77db13e">CreateClusterGroup</a>



<a href="https://msdn.microsoft.com/ac293d5b-edc8-4c5f-9b05-9e2349bf1453">DestroyClusterGroup</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369686(v=VS.85).aspx">Group Management Functions</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

