---
UID: NC:clusapi.PCLUSAPI_SET_CLUSTER_RESOURCE_NAME
title: PCLUSAPI_SET_CLUSTER_RESOURCE_NAME
author: windows-driver-content
description: Sets the name for a resource.
old-location: mscs\setclusterresourcename.htm
old-project: MsCS
ms.assetid: 8525a0b4-d37e-4ed3-8914-2c427978de6c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_RESOURCE_NAME, PCLUSAPI_SET_CLUSTER_RESOURCE_NAME callback, PCLUSAPI_SET_CLUSTER_RESOURCE_NAME callback function [Failover Cluster], _wolf_setclusterresourcename, clusapi/PCLUSAPI_SET_CLUSTER_RESOURCE_NAME, mscs.setclusterresourcename
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_SET_CLUSTER_RESOURCE_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_SET_CLUSTER_RESOURCE_NAME callback function


## -description


Sets the name for a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The 
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
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<i>SetClusterResourceName</i> changes the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> common property of the resource identified by 
    <i>hResource</i>. This is the only way that 
    <b>Name</b>, a read-only property, can be changed.

Do not call <i>SetClusterResourceName</i> from a 
    resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

