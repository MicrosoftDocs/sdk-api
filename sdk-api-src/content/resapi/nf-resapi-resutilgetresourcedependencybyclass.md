---
UID: NF:resapi.ResUtilGetResourceDependencyByClass
title: ResUtilGetResourceDependencyByClass function (resapi.h)
description: Enumerates the dependencies of a specified resource in a specified cluster and returns a handle to a dependency that matches a specified resource class. The PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS","PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS function [Failover Cluster]","ResUtilGetResourceDependencyByClass","ResUtilGetResourceDependencyByClass function [Failover Cluster]","_wolf_resutilgetresourcedependencybyclass","mscs.resutilgetresourcedependencybyclass","resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS","resapi/ResUtilGetResourceDependencyByClass"]
old-location: mscs\resutilgetresourcedependencybyclass.htm
tech.root: MsCS
ms.assetid: 7c2bd24a-8034-4a5f-8218-0a23d5e29b07
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS, PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS function [Failover Cluster], ResUtilGetResourceDependencyByClass, ResUtilGetResourceDependencyByClass function [Failover Cluster], _wolf_resutilgetresourcedependencybyclass, mscs.resutilgetresourcedependencybyclass, resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS, resapi/ResUtilGetResourceDependencyByClass
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
 - ResUtilGetResourceDependencyByClass
 - resapi/ResUtilGetResourceDependencyByClass
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
 - ResUtilGetResourceDependencyByClass
---

# ResUtilGetResourceDependencyByClass function


## -description

Enumerates the  <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a> of a specified  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> in a specified <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to a dependency that matches a specified resource class. The <b>PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to the cluster to which the resource belongs.

### -param hSelf [in]

Handle to the dependent resource. This resource depends on one or more resources.

### -param prci [in]

Pointer to a  <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">CLUS_RESOURCE_CLASS_INFO</a> structure describing the resource class of the dependency to return.

### -param bRecurse [in]

Determines the scope of the search. If <b>TRUE</b>, the function checks the entire dependency tree under the dependent resource. If <b>FALSE</b>, the function checks only the resources on which the dependent resource directly depends.

## -returns

If the operation succeeds, 
the function returns a handle to one of the resources on which the resource specified by <i>hSelf</i> depends. The caller is responsible for closing the handle by calling  <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>.

If the operation fails, the function returns <b>NULL</b>. For more information, call the   <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Do not call  <b>ResUtilGetResourceDependencyByClass</b> from any resource DLL entry point function.  <b>ResUtilGetResourceDependencyByClass</b> can safely be called from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

As the following example illustrates, if you know that resource A depends on a <a href="/previous-versions/windows/desktop/mscs/s-gly">storage class resource</a>, you can use  <b>ResUtilGetResourceDependencyByClass</b> to obtain a handle to the storage class resource without knowing anything else about it.


```cpp
// String initialization and error checking omitted.

HCLUSTER hCluster = OpenCluster( lpszClusterName );

//
// Resource A depends on a storage class resource.
// Get a handle to that resource.
//
HRESOURCE hResA = OpenClusterResource( hCluster, lpszResName );

PCLUS_RESOURCE_CLASS_INFO pClassInfo;

pClassInfo->rc = CLUS_RESCLASS_STORAGE;

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

```

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilfinddependentdiskresourcedriveletter">ResUtilFindDependentDiskResourceDriveLetter</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependency">ResUtilGetResourceDependency</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyname">ResUtilGetResourceDependencyByName</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependentipaddressprops">ResUtilGetResourceDependentIPAddressProps</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a>