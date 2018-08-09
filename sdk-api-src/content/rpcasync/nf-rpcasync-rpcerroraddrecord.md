---
UID: NF:rpcasync.RpcErrorAddRecord
title: RpcErrorAddRecord function
author: windows-sdk-content
description: The RpcErrorAddRecord function adds extended error information to a chain of extended error information records.
old-location: rpc\rpcerroraddrecord.htm
old-project: rpc
ms.assetid: b82708ef-0760-49b0-87d2-3d55a07b351f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RpcErrorAddRecord, RpcErrorAddRecord function [RPC], _rpc_rpcerroraddrecord, rpc.rpcerroraddrecord, rpcasync/RpcErrorAddRecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.typenames: RPC_NOTIFICATION_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcErrorAddRecord
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcErrorAddRecord function


## -description


The 
<b>RpcErrorAddRecord</b> function adds extended error information to a chain of extended error information records.


## -parameters




### -param ErrorInfo [in]

Error information to be added, in the form of an 
<a href="https://msdn.microsoft.com/1e906192-c9f1-41c2-bf7f-9967a3d0e1d3">RPC_EXTENDED_ERROR_INFO</a> structure.


## -returns



Successful completion returns RPC_S_OK.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcErrorAddRecord</b> function enables applications or servers other than the RPC Runtime to add extended error information to a chain of extended error information records.

Responsibility for the strings pointed to by <i>ErrorInfo</i> belong to the caller; the 
<b>RpcErrorAddRecord</b> function makes a copy of those strings, if necessary. The following restrictions on the members of <i>ErrorInfo</i> must be observed:

<b>Version</b> must be set to a valid version, such as RPC_EEINFO_VERSION.

<b>ComputerName</b> must be set to <b>NULL</b>. Any other value results in ERROR_INVALID_PARAMETER.

<b>ProcessID</b> must be set to zero. Any other value results in ERROR_INVALID_PARAMETER.

<b>SystemTime</b> or <b>FileTime</b> is ignored on input, and is set by the RPC Runtime.

<b>GeneratingComponent</b> must be set to zero. Any other value results in ERROR_INVALID_PARAMETER. The RPC Runtime sets this to EEInfoGCApplication.

<b>Status</b> can be set to the error code the caller wants to add to the chain.

<b>DetectionLocation</b> must be set to zero. Any other value results in ERROR_INVALID_PARAMETER.

<b>NumberOfParameters</b> indicates the number of parameters in the Parameters array. This value must be equal or greater than zero or MaxNumberOfEEInfoParams. The RPC Runtime does not use any memory after the specified number of parameters, so callers can safely allocate memory for less than MaxNumberOfEEInfoParams parameters.

<b>Parameters</b> represents the parameters for the extended error information record. The only restriction on Parameters is that <b>Pval</b> is used to represent pointers, and is always 64 bits. Use <b>Pval</b> regardless of whether the system used is 32 bits or 64 bits. Do not use <b>Lval</b>.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/1e906192-c9f1-41c2-bf7f-9967a3d0e1d3">RPC_EXTENDED_ERROR_INFO</a>



<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

