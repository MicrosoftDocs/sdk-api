---
UID: NF:resapi.ResUtilGetResourceDependency
title: ResUtilGetResourceDependency function (resapi.h)
description: Enumerates the dependencies of a specified resource and returns a handle to a dependency of a specified type. The PRESUTIL_GET_RESOURCE_DEPENDENCY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_RESOURCE_DEPENDENCY","PRESUTIL_GET_RESOURCE_DEPENDENCY function [Failover Cluster]","ResUtilGetResourceDependency","ResUtilGetResourceDependency function [Failover Cluster]","_wolf_resutilgetresourcedependency","mscs.resutilgetresourcedependency","resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY","resapi/ResUtilGetResourceDependency"]
old-location: mscs\resutilgetresourcedependency.htm
tech.root: MsCS
ms.assetid: eee267b4-4272-4938-b061-02990ec528f2
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENCY, PRESUTIL_GET_RESOURCE_DEPENDENCY function [Failover Cluster], ResUtilGetResourceDependency, ResUtilGetResourceDependency function [Failover Cluster], _wolf_resutilgetresourcedependency, mscs.resutilgetresourcedependency, resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY, resapi/ResUtilGetResourceDependency
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
 - ResUtilGetResourceDependency
 - resapi/ResUtilGetResourceDependency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-resutils-l1-1-3.dll
 - ResUtils.dll
api_name:
 - ResUtilGetResourceDependency
---

# ResUtilGetResourceDependency function


## -description

Enumerates the  <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a> of a specified  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> and returns a handle to a dependency of a specified type. The <b>PRESUTIL_GET_RESOURCE_DEPENDENCY</b> type defines a pointer to this function.

## -parameters

### -param hSelf [in]

Handle to the dependent resource. This resource depends on one or more resources.

### -param lpszResourceType [in]

Null-terminated Unicode string specifying the resource type of the dependency to return.

## -returns

If the operation succeeds, 
the function returns a handle to one of the resources on which the resource specified by <i>hSelf</i> depends. The caller is responsible for closing the handle by calling  <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>.

If the operation fails, the function returns <b>NULL</b>. For more information, call the   <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The  <b>ResUtilGetResourceDependency</b>,  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyname">ResUtilGetResourceDependencyByName</a>, and  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a> functions are very similar in that they all provide access to dependencies of a particular resource type. The following table summarizes the differences between the functions.

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
<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyname">ResUtilGetResourceDependencyByName</a>
</td>
<td>Resource handle</td>
<td>Yes</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a>
</td>
<td>Resource name</td>
<td>No</td>
</tr>
</table>
 

Do not call  <b>ResUtilGetResourceDependency</b> from any resource DLL entry point function.  <b>ResUtilGetResourceDependency</b> can safely be called from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


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

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfinddependentdiskresourcedriveletter">ResUtilFindDependentDiskResourceDriveLetter</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyclass">ResUtilGetResourceDependencyByClass</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyname">ResUtilGetResourceDependencyByName</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependentipaddressprops">ResUtilGetResourceDependentIPAddressProps</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a>