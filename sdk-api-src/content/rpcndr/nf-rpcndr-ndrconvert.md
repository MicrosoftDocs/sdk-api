---
UID: NF:rpcndr.NdrConvert
title: NdrConvert function
author: windows-sdk-content
description: The NdrConvert function converts the network buffer from the data representation of the sender to the data representation of the receiver if they are different.
old-location: rpc\ndrconvert.htm
tech.root: Rpc
ms.assetid: ee9952c3-04e1-4fc0-a1fb-d50bc60e87f6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NdrConvert, NdrConvert
, NdrConvert function [RPC], rpc.ndrconvert, rpcndr/NdrConvert
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrConvert
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrConvert function


## -description


The <b>NdrConvert</b> function converts the network buffer from the data representation of the sender to the data representation of the receiver if they are different.


## -parameters




### -param pStubMsg [in]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>pRpcMsg</b> member points to a structure whose <b>Buffer</b> member contains the data to convert. This structure is for internal use only and should not be modified.


### -param pFormat [in]

Pointer to type format  of the data to convert.


## -returns



This function has no return values. If an error occurs, the function throws one of the following exception codes.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA or RPC_X_INVALID_BOUND</td>
<td>The network  buffer is incorrect.</td>
</tr>
<tr>
<td>STATUS_ACCESS_VIOLATION</td>
<td>An access violation occurred.</td>
</tr>
<tr>
<td>RPC_S_INTERNAL_ERROR</td>
<td>An error occurred in RPC.</td>
</tr>
</table>
 




## -remarks



The <b>NdrConvert</b> function is used by all <a href="https://msdn.microsoft.com/cf597a45-410f-4098-850b-240c6ebce23b">/Oi</a>, <b>/Oic</b>, and <a href="https://msdn.microsoft.com/dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb">/Os</a> mode  stubs. 



