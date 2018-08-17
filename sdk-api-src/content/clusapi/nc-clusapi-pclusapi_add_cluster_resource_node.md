---
UID: NC:clusapi.PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE
title: PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE
author: windows-sdk-content
description: Adds a node to the list of possible nodes that a resource can run on.
old-location: mscs\addclusterresourcenode.htm
old-project: mscs
ms.assetid: d87f9541-7cc6-4dbb-8f1f-e8e36462b01b
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE, PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE callback, PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE callback function [Failover Cluster], _wolf_addclusterresourcenode, clusapi/PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE, mscs.addclusterresourcenode
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
 - PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_ADD_CLUSTER_RESOURCE_NODE callback function


## -description


Adds a <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> to the list of possible nodes that a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> can run on. The 
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
       <i>AddClusterResourceNode</i> returns one of the 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
    can have additional destructive effects. For information on how LPC and RPC handles are created, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372959(v=VS.85).aspx">Using Object Handles</a> and 
    <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/7658a030-d4b2-407c-829f-61491b5907e6">OpenClusterNode</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>



<a href="https://msdn.microsoft.com/1a5b59b9-5c19-4920-b150-b0b404629fb3">RemoveClusterResourceNode</a>
 

 

