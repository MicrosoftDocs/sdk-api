---
UID: NF:resapi.ResUtilGetResourceNameDependencyEx
title: ResUtilGetResourceNameDependencyEx function (resapi.h)
description: Enumerates the dependencies of a specified resource in the local cluster and returns a handle to a dependency of a specified resource type. The PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX","PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX function [Failover Cluster]","ResUtilGetResourceNameDependencyEx","ResUtilGetResourceNameDependencyEx function [Failover Cluster]","mscs.resutilgetresourcenamedependencyex","resapi/PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX","resapi/ResUtilGetResourceNameDependencyEx"]
old-location: mscs\resutilgetresourcenamedependencyex.htm
tech.root: MsCS
ms.assetid: 3A57C19C-F0A2-4183-ACA6-0CEF2F2FF23E
ms.date: 12/05/2018
ms.keywords: PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX, PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX function [Failover Cluster], ResUtilGetResourceNameDependencyEx, ResUtilGetResourceNameDependencyEx function [Failover Cluster], mscs.resutilgetresourcenamedependencyex, resapi/PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX, resapi/ResUtilGetResourceNameDependencyEx
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
 - ResUtilGetResourceNameDependencyEx
 - resapi/ResUtilGetResourceNameDependencyEx
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
 - ResUtilGetResourceNameDependencyEx
---

# ResUtilGetResourceNameDependencyEx function


## -description

Enumerates the  <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependencies</a> of a specified  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> in the local <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> and returns a handle to a dependency of a specified  <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a>. The <b>PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX</b> type defines a pointer to this function.

## -parameters

### -param lpszResourceName [in]

A null-terminated Unicode string that specifies  the name of the dependent resource. This resource depends on one or more resources.

### -param lpszResourceType [in]

A null-terminated Unicode string that specifies  the resource type of the dependency to return.

### -param dwDesiredAccess [in]

The requested access privileges. This  might be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0), an undefined error  might be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a>.

## -returns

If the operation succeeds, 
the function returns a handle to one of the resources on which the resource that is  specified by <i>lpszResourceName</i> depends. The caller is responsible for closing the handle by calling  <a href="/windows/desktop/api/clusapi/nf-clusapi-closeclusterresource">CloseClusterResource</a>.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>