---
UID: NC:resapi.PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY
title: PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY
author: windows-driver-content
description: Enumerates the dependencies of a specified resource in the local cluster and returns a handle to a dependency of a specified resource type. The PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY type defines a pointer to this function.
old-location: mscs\resutilgetresourcenamedependency.htm
old-project: MsCS
ms.assetid: 071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY, PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY callback, PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY callback function [Failover Cluster], _wolf_resutilgetresourcenamedependency, mscs.resutilgetresourcenamedependency, resapi/PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY callback function


## -description


Enumerates the  <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in the local <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and returns a handle to a dependency of a specified  <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a>. The <b>PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY</b> type defines a pointer to this function.


## -parameters




### -param lpszResourceName [in]

Null-terminated Unicode string specifying the name of the dependent resource. This resource depends on one or more resources.


### -param lpszResourceType [in]

Null-terminated Unicode string specifying the resource type of the dependency to return.


## -returns



If the operation succeeds, 
the function returns a handle to one of the resources on which the resource specified by <i>lpszResourceName</i> depends. The caller is responsible for closing the handle by calling  <a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The  <i>ResUtilGetResourceNameDependency</i>,  <a href="https://msdn.microsoft.com/eee267b4-4272-4938-b061-02990ec528f2">ResUtilGetResourceDependency</a>, and  <a href="https://msdn.microsoft.com/8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57">ResUtilGetResourceDependencyByName</a> functions are very similar in that they all provide access to dependencies of a particular resource type. The following table summarizes the differences between the functions.

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
<td><i>ResUtilGetResourceNameDependency</i></td>
<td>Resource name</td>
<td>No</td>
</tr>
</table>
 

Do not call  <i>ResUtilGetResourceNameDependency</i> from any resource DLL entry point function.  <i>ResUtilGetResourceNameDependency</i> can safely be called from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

As the following example illustrates, if you know that resource A depends on a  <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resource, you can use  <i>ResUtilGetResourceNameDependency</i> to obtain a handle to the dependency.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// String initialization and error checking omitted.

HRESOURCE hResD = ResUtilGetResourceNameDependency(
                        L"Resource_A_Name",
                        L"Physical Disk" );

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



<a href="https://msdn.microsoft.com/8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57">ResUtilGetResourceDependencyByName</a>



<a href="https://msdn.microsoft.com/283b0086-1dbf-45dc-9651-93af9a9ff6d0">ResUtilGetResourceDependentIPAddressProps</a>
 

 

