---
UID: NF:rpcdce.RpcBindingInqOption
title: RpcBindingInqOption function
author: windows-driver-content
description: RPC client processes use RpcBindingInqOption to determine current values of the binding options for a given binding handle.
old-location: rpc\rpcbindinginqoption.htm
old-project: Rpc
ms.assetid: f148c827-d18a-41f2-834a-f6b77b331bcc
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RpcBindingInqOption, RpcBindingInqOption function [RPC], _rpc_rpcbindinginqoption, rpc.rpcbindinginqoption, rpcdce/RpcBindingInqOption
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
req.unicode-ansi: 
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
-	RpcBindingInqOption
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcBindingInqOption function


## -description


RPC client processes use 
<b>RpcBindingInqOption</b> to determine current values of the binding options for a given binding handle.


## -parameters




### -param hBinding

Server binding about which to determine binding-option values.


### -param option

TBD


### -param pOptionValue

Memory location to place the value for the specified <i>Option</i>

<div class="alert"><b>Note</b>  For a list of binding options and their possible values, see 
<a href="https://msdn.microsoft.com/ff88e05d-b9f3-42ef-a44f-fee9261832c8">Binding Option Constants</a>.</div>
<div> </div>

#### - Option

Binding handle property to inquire about.


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
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
The function is not supported for either the operating system or the transport.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Client processes call 
<b>RpcBindingInqOption</b> to determine the current settings of the binding handle options. To inquire about authentication settings clients call the 
<a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a> function. .




## -see-also




<a href="https://msdn.microsoft.com/f1c8665b-3754-4c2e-b3ac-bba1f4b329e1">RPC Message
		  Queuing</a>



<a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a>



<a href="https://msdn.microsoft.com/2db946b6-6a0d-402c-89ef-68c7489aa7ee">RpcBindingSetAuthInfo</a>



<a href="https://msdn.microsoft.com/bc721fb0-2271-4658-995b-a41e8eefc5d5">RpcBindingSetOption</a>



<a href="https://msdn.microsoft.com/ec616bf5-a845-4e7e-9f39-20947d2074f7">message</a>
 

 

