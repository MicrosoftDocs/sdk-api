---
UID: NF:rpcnsi.RpcNsProfileEltInqDone
title: RpcNsProfileEltInqDone function
author: windows-sdk-content
description: The RpcNsProfileEltInqDone function deletes the inquiry context for viewing the elements in a profile.
old-location: rpc\rpcnsprofileeltinqdone.htm
old-project: Rpc
ms.assetid: 957cdfb6-2b5a-4339-8197-897999df5ea0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RpcNsProfileEltInqDone, RpcNsProfileEltInqDone function [RPC], _rpc_rpcnsprofileeltinqdone, rpc.rpcnsprofileeltinqdone, rpcnsi/RpcNsProfileEltInqDone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcnsi.h
req.include-header: Rpc.h
req.redist: 
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
tech.root: 
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsProfileEltInqDone
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: ADAM
---

# RpcNsProfileEltInqDone function


## -description


The 
<b>RpcNsProfileEltInqDone</b> function deletes the inquiry context for viewing the elements in a profile.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param InquiryContext

Pointer to a name-service handle to free. The name-service handle that <i>InquiryContext</i> points to is created by calling the 
<a href="https://msdn.microsoft.com/5b14eb21-0c3e-4f12-b1dc-95b364d87a4f">RpcNsProfileEltInqBegin</a> function. 




An argument value of NULL is returned.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsProfileEltInqDone</b> function frees an inquiry context created by calling 
<a href="https://msdn.microsoft.com/5b14eb21-0c3e-4f12-b1dc-95b364d87a4f">RpcNsProfileEltInqBegin</a>.

An application calls 
<b>RpcNsProfileEltInqDone</b> after viewing profile elements using the 
<a href="https://msdn.microsoft.com/78835fde-82c3-4cff-94b9-91e07120e03f">RpcNsProfileEltInqNext</a> function.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5b14eb21-0c3e-4f12-b1dc-95b364d87a4f">RpcNsProfileEltInqBegin</a>



<a href="https://msdn.microsoft.com/78835fde-82c3-4cff-94b9-91e07120e03f">RpcNsProfileEltInqNext</a>
 

 

