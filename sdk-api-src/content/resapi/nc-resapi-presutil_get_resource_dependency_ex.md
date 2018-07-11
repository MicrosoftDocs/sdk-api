---
UID: NC:resapi.PRESUTIL_GET_RESOURCE_DEPENDENCY_EX
title: PRESUTIL_GET_RESOURCE_DEPENDENCY_EX
author: windows-sdk-content
description: Enumerates the dependencies of a specified resource and returns a handle to a dependency of a specified type. The PRESUTIL_GET_RESOURCE_DEPENDENCY_EX type defines a pointer to this function.
old-location: mscs\resutilgetresourcedependencyex.htm
old-project: mscs
ms.assetid: 8F5BB021-83FB-44CD-94B4-33FC8E398C5B
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PRESUTIL_GET_RESOURCE_DEPENDENCY_EX, PRESUTIL_GET_RESOURCE_DEPENDENCY_EX callback, PRESUTIL_GET_RESOURCE_DEPENDENCY_EX callback function [Failover Cluster], mscs.resutilgetresourcedependencyex, resapi/PRESUTIL_GET_RESOURCE_DEPENDENCY_EX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_GET_RESOURCE_DEPENDENCY_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PRESUTIL_GET_RESOURCE_DEPENDENCY_EX callback function


## -description


Enumerates the  <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> and returns a handle to a dependency of a specified type. The <b>PRESUTIL_GET_RESOURCE_DEPENDENCY_EX</b> type defines a pointer to this function.


## -parameters




### -param hSelf [in]

A handle to the dependent resource.


### -param lpszResourceType [in]

A null-terminated Unicode string that specifies the resource type of the dependency to return.


### -param dwDesiredAccess [in]

The requested access privileges. This  might be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0), an undefined error  might be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="https://msdn.microsoft.com/eee267b4-4272-4938-b061-02990ec528f2">ResUtilGetResourceDependency</a>.


## -returns



If the operation succeeds, 
the function returns a handle to one of the resources on which the resource that is   specified by <i>hSelf</i> depends. The caller is responsible for closing the handle by calling 
the <a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a> function.

If the operation fails, the function returns <b>NULL</b>. For more information, call the   <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/eee267b4-4272-4938-b061-02990ec528f2">ResUtilGetResourceDependency</a>



<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 

