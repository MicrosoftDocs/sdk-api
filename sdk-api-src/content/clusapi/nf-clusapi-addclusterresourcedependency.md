---
UID: NF:clusapi.AddClusterResourceDependency
title: AddClusterResourceDependency function
author: windows-sdk-content
description: Creates a dependency relationship between two resources.
old-location: mscs\addclusterresourcedependency.htm
tech.root: MsCS
ms.assetid: 37f173f3-514e-434b-8531-d308c6233a24
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddClusterResourceDependency, AddClusterResourceDependency function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_RESOURCE_DEPENDENCY, PCLUSAPI_ADD_CLUSTER_RESOURCE_DEPENDENCY function [Failover Cluster], _wolf_addclusterresourcedependency, clusapi/AddClusterResourceDependency, clusapi/PCLUSAPI_ADD_CLUSTER_RESOURCE_DEPENDENCY, mscs.addclusterresourcedependency
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
 - AddClusterResourceDependency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddClusterResourceDependency function


## -description


Creates a <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependency</a> relationship between two 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a>. The <b>PCLUSAPI_ADD_CLUSTER_RESOURCE_DEPENDENCY</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the dependent resource.


### -param hDependsOn [in]

Handle to the resource that the resource identified by <i>hResource</i> should depend 
       on.


## -returns



If the operation succeeds, it returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, 
       <b>AddClusterResourceDependency</b> returns 
       one of the <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following are 
       possible return values.




## -remarks



A dependency relationship created by the 
     <b>AddClusterResourceDependency</b> function 
     affects how resources are moved from one <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to another after a 
     <a href="https://msdn.microsoft.com/f18644d1-63ec-4920-b703-a3f149684508">failure</a>. It determines the order in which resources are 
     taken offline and brought back online.

Resources in a dependency relationship must be moved together. The dependent resource must be brought online 
     after the resource upon which it depends.

The two resources identified by <i>hResource</i> and <i>hDependsOn</i> 
     must be in the same group.

Do not call 
     <b>AddClusterResourceDependency</b> if 
     <i>hResource</i> is already online. The call fails with an 
     <b>ERROR_RESOURCE_ONLINE</b> error. Note that this behavior has changed with Windows Server 2008.  You can call <b>AddClusterResourceDependency</b> and modify resource dependencies without requiring the resource to be brought offline.

Do not call 
     <b>AddClusterResourceDependency</b> from a 
     resource DLL. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/974ec036-3dd3-4453-9ce5-029f58d99d81">CanResourceBeDependent</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>



<a href="https://msdn.microsoft.com/3640ad8d-db0d-4e55-bff0-35fb5d26776f">RemoveClusterResourceDependency</a>
 

 

