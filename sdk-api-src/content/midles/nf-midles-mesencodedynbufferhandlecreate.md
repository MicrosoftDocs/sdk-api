---
UID: NF:midles.MesEncodeDynBufferHandleCreate
title: MesEncodeDynBufferHandleCreate function
author: windows-sdk-content
description: The MesEncodeDynBufferHandleCreate function creates an encoding handle and then initializes it for a dynamic buffer style of serialization.
old-location: rpc\mesencodedynbufferhandlecreate.htm
old-project: Rpc
ms.assetid: 4d8cb8e3-aa5a-4354-87e7-57543baa57e8
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: MesEncodeDynBufferHandleCreate, MesEncodeDynBufferHandleCreate function [RPC], _rpc_mesencodedynbufferhandlecreate, midles/MesEncodeDynBufferHandleCreate, rpc.mesencodedynbufferhandlecreate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	MesEncodeDynBufferHandleCreate
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: GDI+ 1.1
---

# MesEncodeDynBufferHandleCreate function


## -description


The 
<b>MesEncodeDynBufferHandleCreate</b> function creates an encoding handle and then initializes it for a dynamic buffer style of serialization.


## -parameters




### -param pBuffer

TBD


### -param pEncodedSize

Pointer to the size of the completed encoding. The size will be written to the memory location pointed to by <i>pEncodedSize</i> by subsequent encoding operations.


### -param pHandle

Pointer to the address to which the handle will be written.


#### - ppBuffer

Pointer to a pointer to the stub-supplied buffer containing the encoding after serialization is complete.


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
The argument was invalid.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>MesEncodeDynBufferHandleCreate</b> routine is used by applications to allocate the memory and initialize the handle for the dynamic buffer style of encoding. When using the dynamic buffer style of encoding, the buffer into which all the encoded data will be placed is supplied by the stub. This buffer will be allocated by the current client memory-management mechanism.

There can be performance implications when using this style for multiple encodings with the same handle. A single buffer is returned from an encoding and data is copied from intermediate buffers. The buffers are released when necessary.

When a stub is compiled using -protocol all or -protocol ndr64 and the buffer is to be encoded using the NDR64 transfer syntax, the 
MesBufferHandleReset function must be called with its <i>OpCode</i> parameter set to MES_ENCODE_NDR64.




## -see-also




<a href="https://msdn.microsoft.com/adc9681f-267e-4f6f-88a3-ec913e886dd1">MesBufferhandleReset</a>



<a href="https://msdn.microsoft.com/d4a4ac59-56fb-4693-9007-f358105f82f0">MesHandleFree</a>
 

 

