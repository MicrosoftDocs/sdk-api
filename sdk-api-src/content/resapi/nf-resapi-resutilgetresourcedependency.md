---
UID: NF:resapi.ResUtilGetResourceDependency
title: ResUtilGetResourceDependency function (resapi.h)
author: windows-sdk-content
description: Enumerates the dependencies of a specified resource and returns a handle to a dependency of a specified type. The PRESUTIL_GET_RESOURCE_DEPENDENCY type defines a pointer to this function.
old-location: mscs\resutilgetresourcedependency.htm
tech.root: MsCS
ms.assetid: eee267b4-4272-4938-b061-02990ec528f2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENCY, PRESUTIL_GET_RESOURCE_DEPENDENCY function [Failover Cluster], ResUtilGetResourceDependency, ResUtilGetResourceDependency function [Failover Cluster], _wolf_resutilgetresourcedependency, mscs.resutilgetresourcedependency, resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY, resapi/ResUtilGetResourceDependency
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
 - ResUtilGetResourceDependency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetResourceDependency function


## -description


Enumerates the  <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> and returns a handle to a dependency of a specified type. The <b>PRESUTIL_GET_RESOURCE_DEPENDENCY</b> type defines a pointer to this function.


## -parameters




### -param hSelf [in]

Handle to the dependent resource. This resource depends on one or more resources.


### -param lpszResourceType [in]

Null-terminated Unicode string specifying the resource type of the dependency to return.


## -returns



If the operation succeeds, 
the function returns a handle to one of the resources on which the resource specified by <i>hSelf</i> depends. The caller is responsible for closing the handle by calling  <a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>.

If the operation fails, the function returns <b>NULL</b>. For more information, call the   <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The  <b>ResUtilGetResourceDependency</b>,  <a href="https://msdn.microsoft.com/8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57">ResUtilGetResourceDependencyByName</a>, and  <a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a> functions are very similar in that they all provide access to dependencies of a particular resource type. The following table summarizes the differences between the functions.

<table>
<tr>
<th>Function</th>
<th>How the dependent resource is specified</th>
<th>Requires cluster handle</th>
</tr>
<tr>
<td><b>ResUtilGetResourceDependency</b></td>
<td>Resource handle</td>
<td>No</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57">ResUtilGetResourceDependencyByName</a>
</td>
<td>Resource handle</td>
<td>Yes</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a>
</td>
<td>Resource name</td>
<td>No</td>
</tr>
</table>
 

Do not call  <b>ResUtilGetResourceDependency</b> from any resource DLL entry point function.  <b>ResUtilGetResourceDependency</b> can safely be called from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

As the following example illustrates, if you know that resource A depends on a Physical Disk resource, you can use  <b>ResUtilGetResourceDependency</b> to obtain a handle to the dependency.


```cpp
// String initialization and error checking omitted.

HCLUSTER hCluster = OpenCluster( lpszClusterName );

//
// Resource A depends on a Physical Disk resource.
// Get a handle to that resource.
//
HRESOURCE hResA = OpenClusterResource( hCluster, lpszResName );

HRESOURCE hResD = ResUtilGetResourceDependency(
                        hResA,
                        L"Physical Disk" );

// Close handles and free memory.

```





## -see-also




<a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>



<a href="https://msdn.microsoft.com/8f2187e3-6bb7-4756-af2b-a28857581bcb">ResUtilFindDependentDiskResourceDriveLetter</a>



<a href="https://msdn.microsoft.com/7c2bd24a-8034-4a5f-8218-0a23d5e29b07">ResUtilGetResourceDependencyByClass</a>



<a href="https://msdn.microsoft.com/8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57">ResUtilGetResourceDependencyByName</a>



<a href="https://msdn.microsoft.com/283b0086-1dbf-45dc-9651-93af9a9ff6d0">ResUtilGetResourceDependentIPAddressProps</a>



<a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a>
 

 

