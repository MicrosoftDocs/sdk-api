---
UID: NF:midles.MesInqProcEncodingId
title: MesInqProcEncodingId function
author: windows-sdk-content
description: The MesInqProcEncodingId function provides the identity of an encoding.
old-location: rpc\mesinqprocencodingid.htm
tech.root: rpc
ms.assetid: b6d73cc3-cd35-4fe7-87e6-ecbfef777c44
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: MesInqProcEncodingId, MesInqProcEncodingId function [RPC], _rpc_mesinqprocencodingid, midles/MesInqProcEncodingId, rpc.mesinqprocencodingid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: midles.h
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - MesInqProcEncodingId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MesInqProcEncodingId function


## -description


The 
<b>MesInqProcEncodingId</b> function provides the identity of an encoding.


## -parameters




### -param Handle

An encoding or decoding handle.


### -param pInterfaceId

Pointer to the address in which the identity of the interface used to encode the data will be written. The <i>pInterfaceId</i> consists of the interface universally unique identifier 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> and the version number.


### -param pProcNum

Number of the function used to encode the data.


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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNKNOWN_IF</b></dt>
</dl>
</td>
<td width="60%">
Unknown interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_UNSUPPORTED_TRANS_SYN</b></dt>
</dl>
</td>
<td width="60%">
Transfer syntax not supported by server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_INVALID_ES_ACTION</b></dt>
</dl>
</td>
<td width="60%">
Operation for a given handle was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_WRONG_ES_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Incompatible version of the serializing package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_SS_INVALID_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Buffer not valid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>MesInqProcEncodingId</b> function is used by applications to obtain the identity of the function used to encode the data before calling a function to decode it. When called with an encoding handle, it returns the identity of the last encoding operation. When called with a decoding handle, it returns the identity of the next decoding operation by pre-reading the buffer.

This function can only be used to check the identity of a procedure encoding; it cannot be used to check the identity for a type encoding.




## -see-also




<a href="https://msdn.microsoft.com/4d8cb8e3-aa5a-4354-87e7-57543baa57e8">MesEncodeDynBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/7700e0f6-0f30-415c-9873-983ec6c249b2">MesEncodeFixedBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/54bbe560-08a9-4e41-9121-37aab0c209a9">MesEncodeIncrementalHandleCreate</a>
 

 

