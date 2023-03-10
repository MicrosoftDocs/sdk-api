---
UID: NF:resapi.ResUtilGetResourceDependencyByClassEx
title: ResUtilGetResourceDependencyByClassEx function (resapi.h)
description: Enumerates the dependencies of a specified resource in a specified cluster and returns a handle to a dependency that matches a specified resource class. The PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS_EX type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS_EX","PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS_EX function [Failover Cluster]","ResUtilGetResourceDependencyByClassEx","ResUtilGetResourceDependencyByClassEx function [Failover Cluster]","mscs.resutilgetresourcedependencybyclassex","resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS_EX","resapi/ResUtilGetResourceDependencyByClassEx"]
old-location: mscs\resutilgetresourcedependencybyclassex.htm
tech.root: MsCS
ms.assetid: D35816C8-A449-41FF-9398-A6A4E19C29FB
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS_EX, PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS_EX function [Failover Cluster], ResUtilGetResourceDependencyByClassEx, ResUtilGetResourceDependencyByClassEx function [Failover Cluster], mscs.resutilgetresourcedependencybyclassex, resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS_EX, resapi/ResUtilGetResourceDependencyByClassEx
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - ResUtilGetResourceDependencyByClassEx
 - resapi/ResUtilGetResourceDependencyByClassEx
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
 - ResUtilGetResourceDependencyByClassEx
---

# ResUtilGetResourceDependencyByClassEx function


## -description

Enumerates the  <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a> of a specified  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> in a specified <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to a dependency that matches a specified resource class. The <b>PRESUTIL_GET_RESOURCE_DEPENDENCY_BY_CLASS_EX</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

A handle to the cluster to which the resource belongs.

### -param hSelf [in]

A handle to the dependent resource. This resource depends on one or more resources.

### -param prci [in]

A pointer to a  <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_resource_class_info">PCLUS_RESOURCE_CLASS_INFO</a> structure that describes  the resource class of the dependency to return.

### -param bRecurse [in]

Determines the scope of the search. If <b>TRUE</b>, the function checks the entire dependency tree under the dependent resource. If <b>FALSE</b>, the function checks only the resources on which the dependent resource directly depends.

### -param dwDesiredAccess [in]

The requested access privileges. This  might be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0), an undefined error  might be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyclass">ResUtilGetResourceDependencyByClass</a>.

## -returns

If the operation succeeds, 
the function returns a handle to one of the resources on which the resource that is specified by <i>hSelf</i> depends. The caller is responsible for closing the handle by calling  <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>.

If the operation fails, the function returns <b>NULL</b>. For more information, call the   <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>