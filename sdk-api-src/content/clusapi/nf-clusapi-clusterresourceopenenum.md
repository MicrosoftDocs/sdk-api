---
UID: NF:clusapi.ClusterResourceOpenEnum
title: ClusterResourceOpenEnum function
author: windows-sdk-content
description: Opens an enumerator for iterating through a resource's dependencies and nodes.
old-location: mscs\clusterresourceopenenum.htm
tech.root: mscs
ms.assetid: f801401f-f49d-41de-b88b-b832330eeccf
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CLUSTER_RESOURCE_ENUM_DEPENDS, CLUSTER_RESOURCE_ENUM_NODES, CLUSTER_RESOURCE_ENUM_PROVIDES, ClusterResourceOpenEnum, ClusterResourceOpenEnum function [Failover Cluster], PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM, PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM function [Failover Cluster], _wolf_clusterresourceopenenum, clusapi/ClusterResourceOpenEnum, clusapi/PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM, mscs.clusterresourceopenenum
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - ClusterResourceOpenEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterResourceOpenEnum function


## -description


Opens an enumerator for iterating through a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource's</a>
<a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> and 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a>. The <b>PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

A handle to a resource.


### -param dwType [in]

A bitmask that describes the type of <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster objects</a> 
       to be enumerated.


The following values of the 
        <a href="https://msdn.microsoft.com/8b59ab43-7e03-4ddf-82cc-9945e9da6462">CLUSTER_RESOURCE_ENUM</a> enumeration are valid.





#### CLUSTER_RESOURCE_ENUM_DEPENDS (1)

The object is a resource that the resource identified by the <i>hResource</i> parameter 
         directly depends on.



#### CLUSTER_RESOURCE_ENUM_PROVIDES (2)

The object is a resource that depends on the resource identified by <i>hResource</i>.



#### CLUSTER_RESOURCE_ENUM_NODES (4)

The object is a node that can host the resource identified by <i>hResource</i>.


## -returns



If the operation succeeds, the function returns an enumeration handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



Do not call <b>ClusterResourceOpenEnum</b> from 
     any resource DLL entry point function. 
     <b>ClusterResourceOpenEnum</b> can safely be called 
     from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="https://msdn.microsoft.com/391b87d1-6765-45fd-bd27-37a1127e639a">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/49407b45-2b7f-43a2-90ff-98cc557edb31">ClusterResourceCloseEnum</a>



<a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a>
 

 

