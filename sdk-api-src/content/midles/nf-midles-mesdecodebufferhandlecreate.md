---
UID: NF:midles.MesDecodeBufferHandleCreate
title: MesDecodeBufferHandleCreate function
author: windows-sdk-content
description: The MesDecodeBufferHandleCreate function creates a decoding handle and initializes it for a (fixed) buffer style of serialization.
old-location: rpc\mesdecodebufferhandlecreate.htm
tech.root: rpc
ms.assetid: 10a2312d-5969-4dde-bf62-308ad425569b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: MesDecodeBufferHandleCreate, MesDecodeBufferHandleCreate function [RPC], _rpc_mesdecodebufferhandlecreate, midles/MesDecodeBufferHandleCreate, rpc.mesdecodebufferhandlecreate
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
 - MesDecodeBufferHandleCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MesDecodeBufferHandleCreate function


## -description


The 
<b>MesDecodeBufferHandleCreate</b> function creates a decoding handle and initializes it for a (fixed) buffer style of serialization.


## -parameters




### -param Buffer

Pointer to the buffer containing the data to decode.


### -param BufferSize

Bytes of data to decode in the buffer.


### -param pHandle

Pointer to the address to which the handle will be written.


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
<dt><b>RPC_X_INVALID_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer was not valid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>MesDecodeBufferHandleCreate</b> routine is used by applications to create a serialization handle and initialize the handle for the (fixed) buffer style of decoding. When using the fixed buffer style of decoding, the user supplies a single buffer containing all the encoded data. This buffer must have an address which is aligned at 8, and must be a multiple of 8 bytes in size. Further, it must be large enough to hold all of the data to decode.




## -see-also




<a href="https://msdn.microsoft.com/7700e0f6-0f30-415c-9873-983ec6c249b2">MesEncodeFixedBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/d4a4ac59-56fb-4693-9007-f358105f82f0">MesHandleFree</a>
 

 

