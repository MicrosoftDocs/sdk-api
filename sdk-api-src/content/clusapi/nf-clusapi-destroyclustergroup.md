---
UID: NF:clusapi.DestroyClusterGroup
title: DestroyClusterGroup function
author: windows-sdk-content
description: Deletes the specified group from a cluster.
old-location: mscs\destroyclustergroup.htm
tech.root: MsCS
ms.assetid: ac293d5b-edc8-4c5f-9b05-9e2349bf1453
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DestroyClusterGroup, DestroyClusterGroup function [Failover Cluster], PCLUSAPI_DESTROY_CLUSTER_GROUP, PCLUSAPI_DESTROY_CLUSTER_GROUP function [Failover Cluster], clusapi/DestroyClusterGroup, clusapi/PCLUSAPI_DESTROY_CLUSTER_GROUP, mscs.destroyclustergroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - DestroyClusterGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyClusterGroup function


## -description


Deletes the specified <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a> from a 
    <a href="c_gly.htm">cluster</a>. Unlike 
    <a href="https://msdn.microsoft.com/a0a8461c-8919-4620-83a2-bb8e5d03b0c4">DeleteClusterGroup</a> the group can contain resources 
    and it can be online. The <b>PCLUSAPI_DESTROY_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

This parameter takes a handle to the cluster group to be destroyed.


## -returns



This function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If the 
       operation completes successfully the function returns <b>ERROR_SUCCESS</b> (0). Any other 
       returned system error code would indicate that the 
       operation failed.




## -remarks



The <b>PCLUSAPI_DESTROY_CLUSTER_GROUP</b> type defines a pointer to this function.

<b>DestroyClusterGroup</b> does not close the group 
     handle specified by the <i>hGroup</i> parameter. To avoid memory leaks, be sure to close this handle with 
     the <a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a> function.

Do not call <b>DestroyClusterGroup</b> from a resource 
     DLL. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>



<a href="https://msdn.microsoft.com/a0a8461c-8919-4620-83a2-bb8e5d03b0c4">DeleteClusterGroup</a>



<a href="https://msdn.microsoft.com/a2336594-ac24-476e-94e8-460a31c1f643">Group Management Functions</a>
 

 

