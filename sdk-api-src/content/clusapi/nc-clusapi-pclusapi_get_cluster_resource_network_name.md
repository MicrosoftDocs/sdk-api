---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME
title: PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME
author: windows-sdk-content
description: Retrieves the Name private property of the Network Name resource on which a resource is dependent.
old-location: mscs\getclusterresourcenetworkname.htm
old-project: mscs
ms.assetid: db3cdaa6-d686-48be-be4a-468910813d6d
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME, PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME callback, PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME callback function [Failover Cluster], _wolf_getclusterresourcenetworkname, clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME, mscs.getclusterresourcenetworkname
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
 - PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME callback function


## -description


Retrieves the <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> private property of the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371733(v=VS.85).aspx">Network Name</a> resource on 
    which a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> is 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372236(v=VS.85).aspx">dependent</a>. The <b>PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the dependent resource.


### -param lpBuffer [out]

Buffer containing a null-terminated Unicode string that contains the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> private property of the Network Name 
      resource on which the resource depends.


### -param nSize [in, out]

On input, pointer to a count of characters in the buffer pointed to by <i>lpBuffer</i>. 
      On output, pointer to a count of characters in the network name of the Network Name resource contained in the 
      buffer pointed to by <i>lpBuffer</i>, excluding the null-terminating character.


## -returns



If the operation succeeds, the function returns <b>TRUE</b>.

If the operation fails, the function returns <b>FALSE</b>. For more information about the 
       error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Do not call 
    <i>GetClusterResourceNetworkName</i> from any 
    resource DLL entry point function. 
    <i>GetClusterResourceNetworkName</i> can safely 
    be called from a worker thread. For more information, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa372262(v=VS.85).aspx">Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

