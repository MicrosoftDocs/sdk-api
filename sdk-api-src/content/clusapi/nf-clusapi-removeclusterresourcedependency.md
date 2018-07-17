---
UID: NF:clusapi.RemoveClusterResourceDependency
title: RemoveClusterResourceDependency function
author: windows-sdk-content
description: Removes a dependency relationship between two resources.
old-location: mscs\removeclusterresourcedependency.htm
old-project: mscs
ms.assetid: 3640ad8d-db0d-4e55-bff0-35fb5d26776f
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY function [Failover Cluster], RemoveClusterResourceDependency, RemoveClusterResourceDependency function [Failover Cluster], _wolf_removeclusterresourcedependency, clusapi/PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY, clusapi/RemoveClusterResourceDependency, mscs.removeclusterresourcedependency
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - RemoveClusterResourceDependency
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# RemoveClusterResourceDependency function


## -description


Removes a  <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependency</a> relationship between two  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a>. The <b>PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the dependent resource.


### -param hDependsOn [in]

Handle to the resource that the resource identified by <i>hResource</i> currently depends on.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Do not call  <b>RemoveClusterResourceDependency</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and  <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/37f173f3-514e-434b-8531-d308c6233a24">AddClusterResourceDependency</a>



<a href="https://msdn.microsoft.com/974ec036-3dd3-4453-9ce5-029f58d99d81">CanResourceBeDependent</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

