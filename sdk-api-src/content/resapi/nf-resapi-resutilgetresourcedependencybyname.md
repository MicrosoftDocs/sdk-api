---
UID: NF:resapi.ResUtilGetResourceDependencyByName
title: ResUtilGetResourceDependencyByName function
author: windows-sdk-content
description: Enumerates the dependencies of a specified resource in a specified cluster and returns a handle to a dependency of a specified type. The PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME type defines a pointer to this function.
old-location: mscs\resutilgetresourcedependencybyname.htm
tech.root: mscs
ms.assetid: 8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME, PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME function [Failover Cluster], ResUtilGetResourceDependencyByName, ResUtilGetResourceDependencyByName function [Failover Cluster], _wolf_resutilgetresourcedependencybyname, mscs.resutilgetresourcedependencybyname, resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME, resapi/ResUtilGetResourceDependencyByName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: resapi.h
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilGetResourceDependencyByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetResourceDependencyByName function


## -description


Enumerates the  <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in a specified <a href="c_gly.htm">cluster</a> and returns a handle to a dependency of a specified type. The <b>PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the cluster to which the resource belongs.


### -param hSelf [in]

Handle to the dependent resource. This resource depends on one or more resources.


### -param lpszResourceType [in]

NULL-terminated Unicode string specifying the resource type of the dependency to return.


### -param bRecurse [in]

Determines the scope of the search. If <b>TRUE</b>, the function checks the entire dependency tree under the dependent resource. If <b>FALSE</b>, the function checks only the resources on which the dependent resource directly depends.


## -returns



If the operation succeeds, the function returns a handle to one of the resources on which the resource specified by <i>hSelf</i> depends. The caller is responsible for closing the handle by calling  <a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>.

If the operation fails, the function returns <b>NULL</b>. For more information, call the   <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The  <b>ResUtilGetResourceDependencyByName</b>,  <a href="https://msdn.microsoft.com/eee267b4-4272-4938-b061-02990ec528f2">ResUtilGetResourceDependency</a>, and  <a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a> functions are very similar in that they all provide access to dependencies of a particular resource type. The following list summarizes the differences between the functions.

<table>
<tr>
<th>Function</th>
<th>How the dependent resource is specified</th>
<th>Requires cluster handle</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/eee267b4-4272-4938-b061-02990ec528f2">ResUtilGetResourceDependency</a>
</td>
<td>
Resource handle

</td>
<td>
No

</td>
</tr>
<tr>
<td><b>ResUtilGetResourceDependencyByName</b></td>
<td>
Resource handle

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a>
</td>
<td>
Resource name

</td>
<td>
No

</td>
</tr>
</table>
 

Do not call  <b>ResUtilGetResourceDependencyByName</b> from any resource DLL entry point function.  <b>ResUtilGetResourceDependencyByName</b> can safely be called from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

As the following example illustrates, if you know that resource A depends on a Physical Disk resource, you can use  <b>ResUtilGetResourceDependencyByName</b> to obtain a handle to the dependency.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// String initialization and error checking omitted.

HCLUSTER hCluster = OpenCluster( lpszClusterName );

//
// Resource A depends on a storage class resource.
// Get a handle to that resource.
//
HRESOURCE hResA = OpenClusterResource( hCluster, lpszResName );

HRESOURCE hResD = ResUtilGetResourceDependencyByName(
                        hCluster,
                        hResA,
                        L"Physical Disk",
                        TRUE );

// Close handles and free memory.
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>



<a href="https://msdn.microsoft.com/8f2187e3-6bb7-4756-af2b-a28857581bcb">ResUtilFindDependentDiskResourceDriveLetter</a>



<a href="https://msdn.microsoft.com/eee267b4-4272-4938-b061-02990ec528f2">ResUtilGetResourceDependency</a>



<a href="https://msdn.microsoft.com/7c2bd24a-8034-4a5f-8218-0a23d5e29b07">ResUtilGetResourceDependencyByClass</a>



<a href="https://msdn.microsoft.com/283b0086-1dbf-45dc-9651-93af9a9ff6d0">ResUtilGetResourceDependentIPAddressProps</a>



<a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a>
 

 

