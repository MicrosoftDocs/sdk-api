---
UID: NF:clusapi.SetClusterResourceName
title: SetClusterResourceName function
author: windows-sdk-content
description: Sets the name for a resource.
old-location: mscs\setclusterresourcename.htm
tech.root: mscs
ms.assetid: 8525a0b4-d37e-4ed3-8914-2c427978de6c
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PCLUSAPI_SET_CLUSTER_RESOURCE_NAME, PCLUSAPI_SET_CLUSTER_RESOURCE_NAME function [Failover Cluster], SetClusterResourceName, SetClusterResourceName function [Failover Cluster], _wolf_setclusterresourcename, clusapi/PCLUSAPI_SET_CLUSTER_RESOURCE_NAME, clusapi/SetClusterResourceName, mscs.setclusterresourcename
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - SetClusterResourceName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClusterResourceName function


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



<b>SetClusterResourceName</b> changes the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372192(v=VS.85).aspx">Name</a> common property of the resource identified by 
    <i>hResource</i>. This is the only way that 
    <b>Name</b>, a read-only property, can be changed.

Do not call <b>SetClusterResourceName</b> from a 
    resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa372192(v=VS.85).aspx">Name</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

