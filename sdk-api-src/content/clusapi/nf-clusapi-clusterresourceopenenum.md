---
UID: NF:clusapi.ClusterResourceOpenEnum
title: ClusterResourceOpenEnum function
author: windows-sdk-content
description: Opens an enumerator for iterating through a resource's dependencies and nodes.
old-location: mscs\clusterresourceopenenum.htm
tech.root: mscs
ms.assetid: f801401f-f49d-41de-b88b-b832330eeccf
ms.author: windowssdkdev
ms.date: 11/06/2018
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
    <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource's</a>
<a href="https://msdn.microsoft.com/en-us/library/Aa372236(v=VS.85).aspx">dependencies</a> and 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">nodes</a>. The <b>PCLUSAPI_CLUSTER_RESOURCE_OPEN_ENUM</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

A handle to a resource.


### -param dwType [in]

A bitmask that describes the type of <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster objects</a> 
       to be enumerated.


The following values of the 
        <a href="https://msdn.microsoft.com/en-us/library/Bb309166(v=VS.85).aspx">CLUSTER_RESOURCE_ENUM</a> enumeration are valid.





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
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="https://msdn.microsoft.com/en-us/library/Aa369563(v=VS.85).aspx">Enumerating Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa372262(v=VS.85).aspx">Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/49407b45-2b7f-43a2-90ff-98cc557edb31">ClusterResourceCloseEnum</a>



<a href="https://msdn.microsoft.com/73627594-90df-496d-8120-b24c34f13fb5">ClusterResourceEnum</a>
 

 

