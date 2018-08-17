---
UID: NC:clusapi.PCLUSAPI_GET_CLUSTER_RESOURCE_STATE
title: PCLUSAPI_GET_CLUSTER_RESOURCE_STATE
author: windows-sdk-content
description: Returns the current state of a resource.
old-location: mscs\getclusterresourcestate.htm
old-project: mscs
ms.assetid: c3897c96-743e-4753-8fef-b8defe4f2b00
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSAPI_GET_CLUSTER_RESOURCE_STATE, PCLUSAPI_GET_CLUSTER_RESOURCE_STATE callback, PCLUSAPI_GET_CLUSTER_RESOURCE_STATE callback function [Failover Cluster], _wolf_getclusterresourcestate, clusapi/PCLUSAPI_GET_CLUSTER_RESOURCE_STATE, mscs.getclusterresourcestate
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
 - PCLUSAPI_GET_CLUSTER_RESOURCE_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_GET_CLUSTER_RESOURCE_STATE callback function


## -description


Returns 
    the current state of a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a>. The <b>PCLUSAPI_GET_CLUSTER_RESOURCE_STATE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle specifying the resource for which state information should be returned.


### -param lpszNodeName [out, optional]

Pointer to a buffer that receives the name of the specified resource's current owner node as a 
       <b>NULL</b>-terminated Unicode string. Pass <b>NULL</b> if the node name 
       is not required.


### -param lpcchNodeName [in, out, optional]

Pointer to the size of the <i>lpszNodeName</i> buffer as a count of characters. This 
       pointer cannot be <b>NULL</b> unless <i>lpszNodeName</i> is also 
       <b>NULL</b>. On input, specifies the maximum number of characters the buffer can hold, 
       including the terminating <b>NULL</b>. On output, specifies the number of characters in the 
       resulting name, excluding the terminating <b>NULL</b>.


### -param lpszGroupName [out, optional]

Pointer to a buffer that receives the name of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> that 
       contains the specified resource. The name is returned as a <b>NULL</b>-terminated Unicode 
       string. Pass <b>NULL</b> if the group name is not required.


### -param lpcchGroupName [in, out, optional]

Pointer to the size of the <i>lpszGroupName</i> buffer as a count of characters. This 
       pointer cannot be <b>NULL</b> unless <i>lpszNodeName</i> is also 
       <b>NULL</b>. On input, specifies the maximum number of characters the buffer can hold, 
       including the terminating <b>NULL</b>. On output, specifies the number of characters in the 
       resulting name, excluding the terminating <b>NULL</b>.


## -returns



<i>GetClusterResourceState</i> returns the 
       current state of the resource enumerated from the 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309168(v=VS.85).aspx">CLUSTER_RESOURCE_STATE</a> enumeration, which can be 
       represented by one of the following values.




## -remarks



Do not call <i>GetClusterResourceState</i> from 
     any resource DLL entry point function. 
     <i>GetClusterResourceState</i> can safely be called 
     from a worker thread. For more information, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.


#### Examples

See <a href="https://msdn.microsoft.com/en-us/library/Aa369639(v=VS.85).aspx">Getting Object States</a> for an example.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309168(v=VS.85).aspx">CLUSTER_RESOURCE_STATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a>



<a href="https://msdn.microsoft.com/694dbf3d-3355-44d9-8af0-ea2baae832fd">OfflineClusterResource</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>



<a href="https://msdn.microsoft.com/8ea8d741-f6f7-48eb-9678-bbb53f76a9ec">OnlineClusterResource</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

