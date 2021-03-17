---
UID: NF:midles.MesEncodeFixedBufferHandleCreate
title: MesEncodeFixedBufferHandleCreate function (midles.h)
description: The MesEncodeFixedBufferHandleCreate function creates an encoding handle and then initializes it for a fixed buffer style of serialization.
helpviewer_keywords: ["MesEncodeFixedBufferHandleCreate","MesEncodeFixedBufferHandleCreate function [RPC]","_rpc_mesencodefixedbufferhandlecreate","midles/MesEncodeFixedBufferHandleCreate","rpc.mesencodefixedbufferhandlecreate"]
old-location: rpc\mesencodefixedbufferhandlecreate.htm
tech.root: Rpc
ms.assetid: 7700e0f6-0f30-415c-9873-983ec6c249b2
ms.date: 12/05/2018
ms.keywords: MesEncodeFixedBufferHandleCreate, MesEncodeFixedBufferHandleCreate function [RPC], _rpc_mesencodefixedbufferhandlecreate, midles/MesEncodeFixedBufferHandleCreate, rpc.mesencodefixedbufferhandlecreate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MesEncodeFixedBufferHandleCreate
 - midles/MesEncodeFixedBufferHandleCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - MesEncodeFixedBufferHandleCreate
---

# MesEncodeFixedBufferHandleCreate function


## -description

The 
<b>MesEncodeFixedBufferHandleCreate</b> function creates an encoding handle and then initializes it for a fixed buffer style of serialization.

## -parameters

### -param pBuffer

Pointer to the user-supplied buffer.

### -param BufferSize

Size of the user-supplied buffer, in bytes.

### -param pEncodedSize

Pointer to the size of the completed encoding. The size will be written to the pointee by the subsequent encoding operation(s).

### -param pHandle

Pointer to the newly created handle.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>MesEncodeFixedBufferHandleCreate</b> routine is used by applications to create and initialize the handle for the fixed buffer style of encoding. When using the fixed buffer style of encoding, the user supplies a single buffer into which all the encoded data is placed. This buffer must have an address which is aligned at 8, and must be a multiple of 8 bytes in size. Further, it must be large enough to hold an encoding of all the data, along with an encoding header for each routine being encoded.

When the handle is used for multiple encoding operations, the encoded size is cumulative.

When a stub is compiled using <b>-protocol all</b> or <b>-protocol ndr64</b> and the buffer is to be encoded using the NDR64 transfer syntax, the 
<a href="/windows/desktop/api/midles/nf-midles-mesbufferhandlereset">MesBufferHandleReset</a> function must be called with its <i>OpCode</i> parameter set to MES_ENCODE_NDR64.

## -see-also

<a href="/windows/desktop/api/midles/nf-midles-mesbufferhandlereset">MesBufferhandleReset</a>



<a href="/windows/desktop/api/midles/nf-midles-mesdecodebufferhandlecreate">MesDecodeBufferHandleCreate</a>



<a href="/windows/desktop/api/midles/nf-midles-meshandlefree">MesHandleFree</a>