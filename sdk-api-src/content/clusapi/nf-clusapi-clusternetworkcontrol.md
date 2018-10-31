---
UID: NF:clusapi.ClusterNetworkControl
title: ClusterNetworkControl function
author: windows-sdk-content
description: Initiates an operation on a network. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusternetworkcontrol.htm
tech.root: mscs
ms.assetid: df0d7b45-4d8b-4780-944a-0fbba670f99a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ClusterNetworkControl, ClusterNetworkControl function [Failover Cluster], _wolf_clusternetworkcontrol, clusapi/ClusterNetworkControl, mscs.clusternetworkcontrol
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
 - ClusterNetworkControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterNetworkControl function


## -description


Initiates 
    an operation on a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>. The operation performed depends on the 
    <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hNetwork [in]

Handle to the network to be affected by the operation.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> 
       hosting the affected network. If <b>NULL</b>, the local node performs the operation. 
       Specifying <i>hHostNode</i> is optional.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/e9156fc0-688c-4a5b-9c78-91668bf2bd40">network control code</a> specifying the 
       operation to be performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a> and the following 
       topics:


<ul>
<li>
<a href="https://msdn.microsoft.com/c1b20e06-2c1d-4be6-a88c-74cbb2d5abbd">CLUSCTL_NETWORK_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c3ed839-10aa-446d-b71c-61890bcf0499">CLUSCTL_NETWORK_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a1777dd3-656b-473a-a5a0-4fd9de6c0575">CLUSCTL_NETWORK_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9e975325-b700-4f1e-a87a-4c379171f41e">CLUSCTL_NETWORK_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8848668d-e9cc-4e69-ba48-7f7b1972ef40">CLUSCTL_NETWORK_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c6736e29-688f-4a92-8d33-f228f610a1bd">CLUSCTL_NETWORK_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c62818db-0766-4962-a8be-9b64ef348503">CLUSCTL_NETWORK_GET_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/01d0cf8a-7852-4eac-b317-569420791984">CLUSCTL_NETWORK_GET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3b1610a5-d1c9-427a-8431-86e0a7102c92">CLUSCTL_NETWORK_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/56035984-d07c-47a6-b344-2980fb25b0cb">CLUSCTL_NETWORK_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b1ecb5d1-f21e-4353-b20b-13ac7dbdbd7e">CLUSCTL_NETWORK_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c01a8bc5-e2e4-403f-9fe5-fc341fce717e">CLUSCTL_NETWORK_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/25d25a11-930b-4f56-be0c-cbc0691f1a4e">CLUSCTL_NETWORK_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/02e8caf6-525b-4169-9e4f-22e0fd8c33ff">CLUSCTL_NETWORK_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3e708093-d05a-48a6-b8de-38b19422cd25">CLUSCTL_NETWORK_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d33b25e3-c04a-4725-8ace-49c328bd1e99">CLUSCTL_NETWORK_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ae91ab3-04c3-4c68-b248-35d0601ad725">CLUSCTL_NETWORK_VALIDATE_PRIVATE_PROPERTIES</a>
</li>
</ul>



### -param lpInBuffer [in, optional]

Pointer to an input buffer containing information needed for the operation, or <b>NULL</b> 
       if no information is needed.


### -param nInBufferSize [in]

The allocated size (in bytes) of the input buffer.


### -param lpOutBuffer [out, optional]

Pointer to an output buffer to receive the data resulting from the operation, or 
       <b>NULL</b> if no data will be returned.


### -param nOutBufferSize [in]

The allocated size (in bytes) of the output buffer.


### -param lpBytesReturned [in, out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.


## -returns



The function returns one of the following values.




## -remarks



If <b>ClusterNetworkControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i>, and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterNetworkControl</b> is one of the 
     <a href="https://msdn.microsoft.com/89ae667e-6ad9-453e-b370-b3d6a67172a2">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/20f87f60-6237-459a-93bc-f599391e65b0">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9156fc0-688c-4a5b-9c78-91668bf2bd40">Network Control Codes</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

