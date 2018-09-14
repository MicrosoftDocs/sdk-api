---
UID: NF:clusapi.RemoveClusterResourceNode
title: RemoveClusterResourceNode function
author: windows-sdk-content
description: Removes a node from the list of nodes that can host a resource.
old-location: mscs\removeclusterresourcenode.htm
tech.root: mscs
ms.assetid: 1a5b59b9-5c19-4920-b150-b0b404629fb3
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE, PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE function [Failover Cluster], RemoveClusterResourceNode, RemoveClusterResourceNode function [Failover Cluster], _wolf_removeclusterresourcenode, clusapi/PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE, clusapi/RemoveClusterResourceNode, mscs.removeclusterresourcenode
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
 - RemoveClusterResourceNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemoveClusterResourceNode function


## -description


Removes a  <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> from the list of nodes that can host a  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The <b>PCLUSAPI_REMOVE_CLUSTER_RESOURCE_NODE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the target resource.


### -param hNode [in]

Handle to the node that should be removed from the list of potential host nodes belonging to the resource identified by <i>hResource</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



Do not call  <b>RemoveClusterResourceNode</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and  <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/d87f9541-7cc6-4dbb-8f1f-e8e36462b01b">AddClusterResourceNode</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

