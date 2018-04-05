---
UID: NF:clusapi.ClusterNodeControl
title: ClusterNodeControl function
author: windows-driver-content
description: Initiates an operation that affects a node. The operation performed depends on the control code passed to the dwControlCode parameter.
old-location: mscs\clusternodecontrol.htm
old-project: MsCS
ms.assetid: f6fc8525-a2d3-4643-9372-548df5e30900
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ClusterNodeControl, ClusterNodeControl function [Failover Cluster], _wolf_clusternodecontrol, clusapi/ClusterNodeControl, mscs.clusternodecontrol
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClusAPI.dll
api_name:
-	ClusterNodeControl
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterNodeControl function


## -description


Initiates an 
    operation that affects a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>. The operation performed depends on the 
    <a href="https://msdn.microsoft.com/47618915-0985-4415-b7d4-5959fb27eb9f">control code</a> passed to the 
    <i>dwControlCode</i> parameter.


## -parameters




### -param hNode [in]

Handle to the node to be affected.


### -param hHostNode [in, optional]

If non-<b>NULL</b>, handle to the node that will perform the operation instead of the node 
       specified in <i>hNode</i>. If <b>NULL</b>, the node that handles the call 
       performs the operation.


### -param dwControlCode [in]

A <a href="https://msdn.microsoft.com/39b59726-e00e-4011-a7bc-96698e12f1e4">node control code</a> specifying the operation to be 
       performed. For the syntax associated with a control code, refer to  
       <a href="https://msdn.microsoft.com/d107f743-8ce8-4c0c-b7a2-24a70ffbc0f3">Control Code Architecture</a> and the following 
       topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/57b755e2-6f0d-4b06-aca4-6ce57627d8a3">CLUSCTL_NODE_ENUM_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d97ffdfb-50a4-4313-9991-f9223e8bb693">CLUSCTL_NODE_ENUM_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8979b006-5494-4587-9675-983ee9021273">CLUSCTL_NODE_GET_CHARACTERISTICS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5eec9b3b-7f6f-4e28-a0b1-1d5d7db2a9af">CLUSCTL_NODE_GET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a845a925-9725-40e7-b4d7-10cd1a5b5066">CLUSCTL_NODE_GET_COMMON_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f86835e1-2721-46ab-bd85-599e91d1d5bd">CLUSCTL_NODE_GET_FLAGS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0222665c-f029-40d9-b568-b27ad6e78dfc">CLUSCTL_NODE_GET_ID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ad0c5ec-294a-4236-b179-77cafbaa95f2">CLUSCTL_NODE_GET_NAME</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b22f281d-d88d-41bb-ab49-e7168e6e9f95">CLUSCTL_NODE_GET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f66f3966-8364-42be-b59e-b6b9a034c362">CLUSCTL_NODE_GET_PRIVATE_PROPERTY_FMTS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e7466dff-e20e-442e-a91c-b07c34d172d8">CLUSCTL_NODE_GET_RO_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/170509ac-6373-40a4-8370-835bf5d647df">CLUSCTL_NODE_GET_RO_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/753ed089-b5ad-42b4-a947-2504c624f290">CLUSCTL_NODE_SET_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/586b34b5-8da0-4030-922b-95afd3b1204f">CLUSCTL_NODE_SET_PRIVATE_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c52faae4-aadc-4415-8858-d578273a1ecb">CLUSCTL_NODE_UNKNOWN</a>
</li>
<li>
<a href="https://msdn.microsoft.com/edf5e39f-3b56-47c0-b25a-934b0968ccd3">CLUSCTL_NODE_VALIDATE_COMMON_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9e8ebb06-53a5-45cb-b611-dda4c5d01321">CLUSCTL_NODE_VALIDATE_PRIVATE_PROPERTIES</a>
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


### -param lpBytesReturned [out, optional]

Returns the actual size (in bytes) of the data resulting from the operation. If this information is not 
       needed, pass <b>NULL</b> for <i>lpBytesReturned</i>.


## -returns



The function returns one of the following values.




## -remarks



If <b>ClusterNodeControl</b> returns 
     <b>ERROR_MORE_DATA</b>, set <i>nOutBufferSize</i> to the number of bytes 
     pointed to by <i>lpBytesReturned</i> and call the function again.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and 
     can have additional destructive effects. For information on how LPC and RPC handles are created, see 
     <a href="https://msdn.microsoft.com/0fdb2024-9b04-4a38-baf9-3cdabba9bf8c">LPC and RPC Handles</a> and 
     <a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>.

<b>ClusterNodeControl</b> is one of the 
     <a href="https://msdn.microsoft.com/89ae667e-6ad9-453e-b370-b3d6a67172a2">control code functions</a>. For more information on 
     control codes and control code functions, see 
     <a href="https://msdn.microsoft.com/20f87f60-6237-459a-93bc-f599391e65b0">Using Control Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/39b59726-e00e-4011-a7bc-96698e12f1e4">Node Control Codes</a>



<a href="https://msdn.microsoft.com/b2ee2575-cc1e-4696-8e95-9798fb556c58">OpenCluster</a>
 

 

