---
UID: NF:clusapi.GetClusterResourceNetworkName
title: GetClusterResourceNetworkName function
author: windows-sdk-content
description: Retrieves the Name private property of the Network Name resource on which a resource is dependent.
old-location: mscs\getclusterresourcenetworkname.htm
tech.root: mscs
ms.assetid: db3cdaa6-d686-48be-be4a-468910813d6d
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: GetClusterResourceNetworkName, GetClusterResourceNetworkName function [Failover Cluster], PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME, PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME function [Failover Cluster], _wolf_getclusterresourcenetworkname, clusapi/GetClusterResourceNetworkName, clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME, mscs.getclusterresourcenetworkname
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
api_name:
 - GetClusterResourceNetworkName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetClusterResourceNetworkName function


## -description


Retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa371735(v=VS.85).aspx">Name</a> private property of the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa371733(v=VS.85).aspx">Network Name</a> resource on 
    which a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> is 
    <a href="https://msdn.microsoft.com/en-us/library/Aa372236(v=VS.85).aspx">dependent</a>. The <b>PCLUSAPI_GET_CLUSTER_RESOURCE_NETWORK_NAME</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the dependent resource.


### -param lpBuffer [out]

Buffer containing a null-terminated Unicode string that contains the 
      <a href="https://msdn.microsoft.com/en-us/library/Aa371735(v=VS.85).aspx">Name</a> private property of the Network Name 
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
    <b>GetClusterResourceNetworkName</b> from any 
    resource DLL entry point function. 
    <b>GetClusterResourceNetworkName</b> can safely 
    be called from a worker thread. For more information, see 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa372262(v=VS.85).aspx">Cluster Resource Management Functions</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

