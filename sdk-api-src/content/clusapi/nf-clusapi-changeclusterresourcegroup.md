---
UID: NF:clusapi.ChangeClusterResourceGroup
title: ChangeClusterResourceGroup function
author: windows-sdk-content
description: Moves a resource from one group to another.
old-location: mscs\changeclusterresourcegroup.htm
tech.root: MsCS
ms.assetid: 99720615-ad5d-4d9a-a6ae-8ba1cd2499f2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ChangeClusterResourceGroup, ChangeClusterResourceGroup function [Failover Cluster], PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP, PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP function [Failover Cluster], _wolf_changeclusterresourcegroup, clusapi/ChangeClusterResourceGroup, clusapi/PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP, mscs.changeclusterresourcegroup
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
 - ChangeClusterResourceGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ChangeClusterResourceGroup function


## -description


Moves a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from one 
    <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a> to another. The 
    <b>PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle of the resource to be moved.


### -param hGroup [in]

Handle of the group that should receive the resource identified by 
      <i>hResource</i>.


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



With the <b>ChangeClusterResourceGroup</b> 
    function, both the group that a resource currently belongs to and its new group must be owned by the same 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> regardless of the resource's state.

Do not call <b>ChangeClusterResourceGroup</b> 
    from a resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>. 
    If the resource identified by <i>hResource</i> has 
    <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a>, all of the resources in its dependency 
    tree are moved to the group identified by <i>hGroup</i>. For example, in the situation shown 
    in the following diagram, changing resource B to group 2 will move the entire dependency tree (resources A, X, and 
    Y) .

<img alt="" border="0" src="./images/resmove.png"/>
Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
    can have additional destructive effects. For information on how LPC and RPC handles are created, see 
    <a href="https://msdn.microsoft.com/709effda-5ff1-439e-805a-9169ca63c182">Using Object Handles</a> and 
    <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

