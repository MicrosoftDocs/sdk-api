---
UID: NF:rpcnsi.RpcNsEntryObjectInqDone
title: RpcNsEntryObjectInqDone function
author: windows-driver-content
description: The RpcNsEntryObjectInqDone function deletes the inquiry context for a name-service database entry's objects.
old-location: rpc\rpcnsentryobjectinqdone.htm
old-project: Rpc
ms.assetid: de1ed214-1018-498a-81a9-7932d4eead0b
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: RpcNsEntryObjectInqDone, RpcNsEntryObjectInqDone function [RPC], _rpc_rpcnsentryobjectinqdone, rpc.rpcnsentryobjectinqdone, rpcnsi/RpcNsEntryObjectInqDone
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
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcns4.dll
api_name:
-	RpcNsEntryObjectInqDone
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcNsEntryObjectInqDone function


## -description


The 
<b>RpcNsEntryObjectInqDone</b> function deletes the inquiry context for a name-service database entry's objects.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param InquiryContext

Pointer to a name-service handle specifying the object UUIDs exported to the <i>EntryName</i> parameter specified in the 
<a href="https://msdn.microsoft.com/dc667dc3-0812-43d5-adc2-aa29ee67f045">RpcNsEntryObjectInqBegin</a> function. 




An argument value of <b>NULL</b> is returned.


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
<b>RpcNsEntryObjectInqDone</b> function frees an inquiry context created by calling the 
<a href="https://msdn.microsoft.com/dc667dc3-0812-43d5-adc2-aa29ee67f045">RpcNsEntryObjectInqBegin</a> function.

An application calls 
<b>RpcNsEntryObjectInqDone</b> after viewing exported object UUIDs using the 
<a href="https://msdn.microsoft.com/95648480-5b53-4a8c-ba82-6c7f204520d2">RpcNsEntryObjectInqNext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/dc667dc3-0812-43d5-adc2-aa29ee67f045">RpcNsEntryObjectInqBegin</a>



<a href="https://msdn.microsoft.com/95648480-5b53-4a8c-ba82-6c7f204520d2">RpcNsEntryObjectInqNext</a>
 

 

