---
UID: NF:clusapi.RemoveClusterResourceDependency
title: RemoveClusterResourceDependency function
author: windows-sdk-content
description: Removes a dependency relationship between two resources.
old-location: mscs\removeclusterresourcedependency.htm
tech.root: MsCS
ms.assetid: 3640ad8d-db0d-4e55-bff0-35fb5d26776f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY, PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY function [Failover Cluster], RemoveClusterResourceDependency, RemoveClusterResourceDependency function [Failover Cluster], _wolf_removeclusterresourcedependency, clusapi/PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY, clusapi/RemoveClusterResourceDependency, mscs.removeclusterresourcedependency
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
 - RemoveClusterResourceDependency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemoveClusterResourceDependency function


## -description


Removes a  <a href="https://msdn.microsoft.com/en-us/library/Aa372236(v=VS.85).aspx">dependency</a> relationship between two  <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a>. The <b>PCLUSAPI_REMOVE_CLUSTER_RESOURCE_DEPENDENCY</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the dependent resource.


### -param hDependsOn [in]

Handle to the resource that the resource identified by <i>hResource</i> currently depends on.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



Do not call  <b>RemoveClusterResourceDependency</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://msdn.microsoft.com/en-us/library/Aa372959(v=VS.85).aspx">Using Object Handles</a> and  <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/37f173f3-514e-434b-8531-d308c6233a24">AddClusterResourceDependency</a>



<a href="https://msdn.microsoft.com/974ec036-3dd3-4453-9ce5-029f58d99d81">CanResourceBeDependent</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

