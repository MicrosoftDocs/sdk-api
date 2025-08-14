---
UID: NF:resapi.ResUtilGetResourceNameDependency
title: ResUtilGetResourceNameDependency function (resapi.h)
description: Enumerates the dependencies of a specified resource in the local cluster and returns a handle to a dependency of a specified resource type. The PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY","PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY function [Failover Cluster]","ResUtilGetResourceNameDependency","ResUtilGetResourceNameDependency function [Failover Cluster]","_wolf_resutilgetresourcenamedependency","mscs.resutilgetresourcenamedependency","resapi/PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY","resapi/ResUtilGetResourceNameDependency"]
old-location: mscs\resutilgetresourcenamedependency.htm
tech.root: MsCS
ms.assetid: 071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY, PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY function [Failover Cluster], ResUtilGetResourceNameDependency, ResUtilGetResourceNameDependency function [Failover Cluster], _wolf_resutilgetresourcenamedependency, mscs.resutilgetresourcenamedependency, resapi/PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY, resapi/ResUtilGetResourceNameDependency
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
 - ResUtilGetResourceNameDependency
 - resapi/ResUtilGetResourceNameDependency
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
 - ResUtilGetResourceNameDependency
---

# ResUtilGetResourceNameDependency function


## -description

Enumerates the  <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a> of a specified  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> in the local <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to a dependency of a specified  <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a>. The <b>PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY</b> type defines a pointer to this function.

## -parameters

### -param lpszResourceName [in]

Null-terminated Unicode string specifying the name of the dependent resource. This resource depends on one or more resources.

### -param lpszResourceType [in]

Null-terminated Unicode string specifying the resource type of the dependency to return.

## -returns

If the operation succeeds, 
the function returns a handle to one of the resources on which the resource specified by <i>lpszResourceName</i> depends. The caller is responsible for closing the handle by calling  <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The  <b>ResUtilGetResourceNameDependency</b>,  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependency">ResUtilGetResourceDependency</a>, and  <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyname">ResUtilGetResourceDependencyByName</a> functions are very similar in that they all provide access to dependencies of a particular resource type. The following table summarizes the differences between the functions.

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
<td><b>ResUtilGetResourceNameDependency</b></td>
<td>Resource name</td>
<td>No</td>
</tr>
</table>
 

Do not call  <b>ResUtilGetResourceNameDependency</b> from any resource DLL entry point function.  <b>ResUtilGetResourceNameDependency</b> can safely be called from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

As the following example illustrates, if you know that resource A depends on a  <a href="/previous-versions/windows/desktop/mscs/physical-disk">Physical Disk</a> resource, you can use  <b>ResUtilGetResourceNameDependency</b> to obtain a handle to the dependency.


```cpp
// String initialization and error checking omitted.

HRESOURCE hResD = ResUtilGetResourceNameDependency(
                        L"Resource_A_Name",
                        L"Physical Disk" );

// Close handles and free memory.

```

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfinddependentdiskresourcedriveletter">ResUtilFindDependentDiskResourceDriveLetter</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependency">ResUtilGetResourceDependency</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyclass">ResUtilGetResourceDependencyByClass</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyname">ResUtilGetResourceDependencyByName</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependentipaddressprops">ResUtilGetResourceDependentIPAddressProps</a>