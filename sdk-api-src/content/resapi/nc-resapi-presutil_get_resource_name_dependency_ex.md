---
UID: NC:resapi.PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX
title: PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX
author: windows-sdk-content
description: Enumerates the dependencies of a specified resource in the local cluster and returns a handle to a dependency of a specified resource type. The PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX type defines a pointer to this function.
old-location: mscs\resutilgetresourcenamedependencyex.htm
old-project: MsCS
ms.assetid: 3A57C19C-F0A2-4183-ACA6-0CEF2F2FF23E
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX, PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX callback, PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX callback function [Failover Cluster], mscs.resutilgetresourcenamedependencyex, resapi/PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX callback function


## -description


Enumerates the  <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> of a specified  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> in the local <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and returns a handle to a dependency of a specified  <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a>. The <b>PRESUTIL_GET_RESOURCE_NAME_DEPENDENCY_EX</b> type defines a pointer to this function.


## -parameters




### -param lpszResourceName [in]

A null-terminated Unicode string that specifies  the name of the dependent resource. This resource depends on one or more resources.


### -param lpszResourceType [in]

A null-terminated Unicode string that specifies  the resource type of the dependency to return.


### -param dwDesiredAccess [in]

The requested access privileges. This  might be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0), an undefined error  might be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a>.


## -returns



If the operation succeeds, 
the function returns a handle to one of the resources on which the resource that is  specified by <i>lpszResourceName</i> depends. The caller is responsible for closing the handle by calling  <a href="https://msdn.microsoft.com/dbefd7f9-3499-45b3-a5c8-d0000632f61c">CloseClusterResource</a>.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call the function  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 

