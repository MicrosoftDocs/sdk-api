---
UID: NF:resapi.ResUtilGetResourceDependencyByName
title: ResUtilGetResourceDependencyByName function (resapi.h)
description: Enumerates the dependencies of a specified resource in a specified cluster and returns a handle to a dependency of a specified type. The PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME","PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME function [Failover Cluster]","ResUtilGetResourceDependencyByName","ResUtilGetResourceDependencyByName function [Failover Cluster]","_wolf_resutilgetresourcedependencybyname","mscs.resutilgetresourcedependencybyname","resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME","resapi/ResUtilGetResourceDependencyByName"]
old-location: mscs\resutilgetresourcedependencybyname.htm
tech.root: MsCS
ms.assetid: 8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME, PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME function [Failover Cluster], ResUtilGetResourceDependencyByName, ResUtilGetResourceDependencyByName function [Failover Cluster], _wolf_resutilgetresourcedependencybyname, mscs.resutilgetresourcedependencybyname, resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME, resapi/ResUtilGetResourceDependencyByName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilGetResourceDependencyByName
 - resapi/ResUtilGetResourceDependencyByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilGetResourceDependencyByName
---

# ResUtilGetResourceDependencyByName function


## -description

Enumerates the  <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a> of a specified  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> in a specified <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to a dependency of a specified type. The <b>PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_NAME</b> type defines a pointer to this function.

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

If the operation succeeds, the function returns a handle to one of the resources on which the resource specified by <i>hSelf</i> depends. The caller is responsible for closing the handle by calling  <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>.

If the operation fails, the function returns <b>NULL</b>. For more information, call the   <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESOURCE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information, call the function  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>

## -remarks

The  <b>ResUtilGetResourceDependencyByName</b>,  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependency">ResUtilGetResourceDependency</a>, and  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a> functions are very similar in that they all provide access to dependencies of a particular resource type. The following list summarizes the differences between the functions.

<table>
<tr>
<th>Function</th>
<th>How the dependent resource is specified</th>
<th>Requires cluster handle</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependency">ResUtilGetResourceDependency</a>
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
<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a>
</td>
<td>
Resource name

</td>
<td>
No

</td>
</tr>
</table>
 

Do not call  <b>ResUtilGetResourceDependencyByName</b> from any resource DLL entry point function.  <b>ResUtilGetResourceDependencyByName</b> can safely be called from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

As the following example illustrates, if you know that resource A depends on a Physical Disk resource, you can use  <b>ResUtilGetResourceDependencyByName</b> to obtain a handle to the dependency.


```cpp
// String initialization and error checking omitted.

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

```

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfinddependentdiskresourcedriveletter">ResUtilFindDependentDiskResourceDriveLetter</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependency">ResUtilGetResourceDependency</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyclass">ResUtilGetResourceDependencyByClass</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependentipaddressprops">ResUtilGetResourceDependentIPAddressProps</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a>