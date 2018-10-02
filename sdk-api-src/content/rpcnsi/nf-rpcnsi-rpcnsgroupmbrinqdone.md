---
UID: NF:rpcnsi.RpcNsGroupMbrInqDone
title: RpcNsGroupMbrInqDone function
author: windows-sdk-content
description: The RpcNsGroupMbrInqDone function deletes the inquiry context for a group.
old-location: rpc\rpcnsgroupmbrinqdone.htm
tech.root: Rpc
ms.assetid: fe40be4d-1468-429a-aa20-694467076bde
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RpcNsGroupMbrInqDone, RpcNsGroupMbrInqDone function [RPC], _rpc_rpcnsgroupmbrinqdone, rpc.rpcnsgroupmbrinqdone, rpcnsi/RpcNsGroupMbrInqDone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcnsi.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsGroupMbrInqDone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcNsGroupMbrInqDone function


## -description


The 
<b>RpcNsGroupMbrInqDone</b> function deletes the inquiry context for a group.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param InquiryContext

Pointer to a name-service handle to free. A value of NULL is returned.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_NS_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The name-service handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsGroupMbrInqDone</b> function frees an inquiry context created by calling the 
<a href="https://msdn.microsoft.com/f3a98563-0c7f-4f4b-b272-af7c0366b95d">RpcNsGroupMbrInqBegin</a> function. An application calls 
<b>RpcNsGroupMbrInqDone</b> after viewing RPC group members using the 
<a href="https://msdn.microsoft.com/58f32594-85de-4d20-86b2-210367ccb7ce">RpcNsGroupMbrInqNext</a> function.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f3a98563-0c7f-4f4b-b272-af7c0366b95d">RpcNsGroupMbrInqBegin</a>



<a href="https://msdn.microsoft.com/58f32594-85de-4d20-86b2-210367ccb7ce">RpcNsGroupMbrInqNext</a>
 

 

