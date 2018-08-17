---
UID: NF:clusapi.ChangeClusterResourceGroup
title: ChangeClusterResourceGroup function
author: windows-sdk-content
description: Moves a resource from one group to another.
old-location: mscs\changeclusterresourcegroup.htm
old-project: mscs
ms.assetid: 99720615-ad5d-4d9a-a6ae-8ba1cd2499f2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ChangeClusterResourceGroup, ChangeClusterResourceGroup function [Failover Cluster], PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP, PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP function [Failover Cluster], _wolf_changeclusterresourcegroup, clusapi/ChangeClusterResourceGroup, clusapi/PCLUSAPI_CHANGE_CLUSTER_RESOURCE_GROUP, mscs.changeclusterresourcegroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.redist: 
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
api_name:
 - ChangeClusterResourceGroup
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ChangeClusterResourceGroup function


## -description


Moves a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> from one 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a> to another. The 
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
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



With the <b>ChangeClusterResourceGroup</b> 
    function, both the group that a resource currently belongs to and its new group must be owned by the same 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> regardless of the resource's state.

Do not call <b>ChangeClusterResourceGroup</b> 
    from a resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>. 
    If the resource identified by <i>hResource</i> has 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372236(v=VS.85).aspx">dependencies</a>, all of the resources in its dependency 
    tree are moved to the group identified by <i>hGroup</i>. For example, in the situation shown 
    in the following diagram, changing resource B to group 2 will move the entire dependency tree (resources A, X, and 
    Y) .

<img alt="" border="0" src="images/resmove.png"/>
Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
    can have additional destructive effects. For information on how LPC and RPC handles are created, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372959(v=VS.85).aspx">Using Object Handles</a> and 
    <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

