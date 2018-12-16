---
UID: NF:clusapi.AddClusterResourceNode
title: AddClusterResourceNode function
author: windows-sdk-content
description: Adds a node to the list of possible nodes that a resource can run on.
old-location: mscs\addclusterresourcenode.htm
tech.root: mscs
ms.assetid: d87f9541-7cc6-4dbb-8f1f-e8e36462b01b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddClusterResourceNode, AddClusterResourceNode function [Failover Cluster], PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE, PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE function [Failover Cluster], _wolf_addclusterresourcenode, clusapi/AddClusterResourceNode, clusapi/PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE, mscs.addclusterresourcenode
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
 - AddClusterResourceNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddClusterResourceNode function


## -description


Adds a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to the list of possible nodes that a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> can run on. The 
    <b>PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to a resource that will add a node to its possible owners list.


### -param hNode [in]

Handle to the node to be added to the list of potential host nodes belonging to the resource identified by 
      <i>hResource</i>.


## -returns



If the operation succeeds, it returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
       <b>AddClusterResourceNode</b> returns one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
    can have additional destructive effects. For information on how LPC and RPC handles are created, see 
    <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and 
    <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>



<a href="https://msdn.microsoft.com/1a5b59b9-5c19-4920-b150-b0b404629fb3">RemoveClusterResourceNode</a>
 

 

