---
UID: NF:rpcdce.RpcStringFree
title: RpcStringFree function
author: windows-driver-content
description: The RpcStringFree function frees a character string allocated by the RPC run-time library.
old-location: rpc\rpcstringfree.htm
old-project: Rpc
ms.assetid: 07226282-1091-4479-adc8-b2f604c645e7
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RpcStringFree, RpcStringFree function [RPC], RpcStringFreeA, RpcStringFreeW, _rpc_rpcstringfree, rpc.rpcstringfree, rpcdce/RpcStringFree, rpcdce/RpcStringFreeA, rpcdce/RpcStringFreeW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcStringFreeW (Unicode) and RpcStringFreeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcStringFree
-	RpcStringFreeA
-	RpcStringFreeW
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcStringFree function


## -description


The 
<b>RpcStringFree</b> function frees a character string allocated by the RPC run-time library.


## -parameters




### -param String

Pointer to a pointer to the character string to free.


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



An application is responsible for calling 
<b>RpcStringFree</b> once for each character string allocated and returned by calls to other RPC run-time library routines.




## -see-also




<a href="https://msdn.microsoft.com/fd4fea9a-067e-4a1b-8be5-867bbe9663c5">RpcBindingToStringBinding</a>



<a href="https://msdn.microsoft.com/fff87506-4c3f-47cb-8130-78e46e906bf0">RpcNsBindingInqEntryName</a>



<a href="https://msdn.microsoft.com/c55d0259-e251-42d0-8565-ce71ab3bb59c">RpcStringBindingParse</a>
 

 

