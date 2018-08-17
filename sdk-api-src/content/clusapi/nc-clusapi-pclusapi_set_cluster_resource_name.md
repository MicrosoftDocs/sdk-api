---
UID: NC:clusapi.PCLUSAPI_SET_CLUSTER_RESOURCE_NAME
title: PCLUSAPI_SET_CLUSTER_RESOURCE_NAME
author: windows-sdk-content
description: Sets the name for a resource.
old-location: mscs\setclusterresourcename.htm
old-project: mscs
ms.assetid: 8525a0b4-d37e-4ed3-8914-2c427978de6c
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_RESOURCE_NAME, PCLUSAPI_SET_CLUSTER_RESOURCE_NAME callback, PCLUSAPI_SET_CLUSTER_RESOURCE_NAME callback function [Failover Cluster], _wolf_setclusterresourcename, clusapi/PCLUSAPI_SET_CLUSTER_RESOURCE_NAME, mscs.setclusterresourcename
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: clusapi.h
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_SET_CLUSTER_RESOURCE_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_SET_CLUSTER_RESOURCE_NAME callback function


## -description


Sets the name for a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a>. The 
    <b>PCLUSAPI_SET_CLUSTER_RESOURCE_NAME</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to a resource to rename.


### -param lpszResourceName [in]

Pointer to the new name for the resource identified by <i>hResource</i>. Resource names 
      are not case sensitive. A resource name must be unique within the cluster.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



<i>SetClusterResourceName</i> changes the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> common property of the resource identified by 
    <i>hResource</i>. This is the only way that 
    <b>Name</b>, a read-only property, can be changed.

Do not call <i>SetClusterResourceName</i> from a 
    resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

