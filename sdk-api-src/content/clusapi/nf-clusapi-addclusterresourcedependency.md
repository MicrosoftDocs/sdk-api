---
UID: NF:clusapi.AddClusterResourceDependency
title: AddClusterResourceDependency function
author: windows-sdk-content
description: Creates a dependency relationship between two resources.
old-location: mscs\addclusterresourcedependency.htm
tech.root: mscs
ms.assetid: 37f173f3-514e-434b-8531-d308c6233a24
ms.author: windowssdkdev
ms.date: 12/5/2018
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


Creates a <a href="https://msdn.microsoft.com/en-us/library/Aa372236(v=VS.85).aspx">dependency</a> relationship between two 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a>. The <b>PCLUSAPI_ADD_CLUSTER_RESOURCE_DEPENDENCY</b> type defines a pointer to this function.


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
       one of the <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>. The following are 
       possible return values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CIRCULAR_DEPENDENCY</b></dt>
<dt>1059 (0x423)</dt>
</dl>
</td>
<td width="60%">
A resource depends on itself.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEPENDENCY_ALREADY_EXISTS</b></dt>
<dt>5003 (0x138B)</dt>
</dl>
</td>
<td width="60%">
The resource dependency already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEPENDENCY_NOT_ALLOWED</b></dt>
<dt>5069 (0x13CD)</dt>
</dl>
</td>
<td width="60%">
The dependent resource is the quorum.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87 (0x57)</dt>
</dl>
</td>
<td width="60%">
The resources are not in the same group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_NOT_AVAILABLE</b></dt>
<dt>5006 (0x138E)</dt>
</dl>
</td>
<td width="60%">
At least one of the resources is marked for deletion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_ONLINE</b></dt>
<dt>5019 (0x139B)</dt>
</dl>
</td>
<td width="60%">
The dependent resource is already online.

</td>
</tr>
</table>
 




## -remarks



A dependency relationship created by the 
     <b>AddClusterResourceDependency</b> function 
     affects how resources are moved from one <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a> to another after a 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372255(v=VS.85).aspx">failure</a>. It determines the order in which resources are 
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
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa372959(v=VS.85).aspx">Using Object Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.




## -see-also




<a href="https://msdn.microsoft.com/974ec036-3dd3-4453-9ce5-029f58d99d81">CanResourceBeDependent</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>



<a href="https://msdn.microsoft.com/3640ad8d-db0d-4e55-bff0-35fb5d26776f">RemoveClusterResourceDependency</a>
 

 

