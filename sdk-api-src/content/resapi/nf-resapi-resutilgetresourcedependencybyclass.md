---
UID: NF:resapi.ResUtilGetResourceDependencyByClass
title: ResUtilGetResourceDependencyByClass function
author: windows-sdk-content
description: Enumerates the dependencies of a specified resource in a specified cluster and returns a handle to a dependency that matches a specified resource class. The PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS type defines a pointer to this function.
old-location: mscs\resutilgetresourcedependencybyclass.htm
tech.root: MsCS
ms.assetid: 7c2bd24a-8034-4a5f-8218-0a23d5e29b07
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS, PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS function [Failover Cluster], ResUtilGetResourceDependencyByClass, ResUtilGetResourceDependencyByClass function [Failover Cluster], _wolf_resutilgetresourcedependencybyclass, mscs.resutilgetresourcedependencybyclass, resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS, resapi/ResUtilGetResourceDependencyByClass
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
 - ResUtilGetResourceDependencyByClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilGetResourceDependencyByClass function


## -description


Enumerates the  <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in a specified <a href="c_gly.htm">cluster</a> and returns a handle to a dependency that matches a specified resource class. The <b>PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Handle to the cluster to which the resource belongs.


### -param hSelf [in]

Handle to the dependent resource. This resource depends on one or more resources.


### -param prci [in]

Pointer to a  <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure describing the resource class of the dependency to return.


### -param bRecurse [in]

Determines the scope of the search. If <b>TRUE</b>, the function checks the entire dependency tree under the dependent resource. If <b>FALSE</b>, the function checks only the resources on which the dependent resource directly depends.


## -returns



If the operation succeeds, 
the function returns a handle to one of the resources on which the resource specified by <i>hSelf</i> depends. The caller is responsible for closing the handle by calling  <a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>.

If the operation fails, the function returns <b>NULL</b>. For more information, call the   <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



Do not call  <b>ResUtilGetResourceDependencyByClass</b> from any resource DLL entry point function.  <b>ResUtilGetResourceDependencyByClass</b> can safely be called from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

As the following example illustrates, if you know that resource A depends on a <a href="s_gly.htm">storage class resource</a>, you can use  <b>ResUtilGetResourceDependencyByClass</b> to obtain a handle to the storage class resource without knowing anything else about it.

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

PCLUS_RESOURCE_CLASS_INFO pClassInfo;

pClassInfo-&gt;rc = CLUS_RESCLASS_STORAGE;

//
// Returns a handle to the storage class resource on which resource A depends.
// Can now perform a variety of operations on the dependency.
//
HRESOURCE hResD = ResUtilGetResourceDependencyByClass(
                        hCluster,
                        hResA,
                        pClassInfo,
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



<a href="https://msdn.microsoft.com/8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57">ResUtilGetResourceDependencyByName</a>



<a href="https://msdn.microsoft.com/283b0086-1dbf-45dc-9651-93af9a9ff6d0">ResUtilGetResourceDependentIPAddressProps</a>



<a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a>
 

 

