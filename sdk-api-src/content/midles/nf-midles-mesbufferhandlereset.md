---
UID: NF:midles.MesBufferHandleReset
title: MesBufferHandleReset function (midles.h)
description: The MesBufferHandleReset function re-initializes the handle for buffer serialization.
helpviewer_keywords: ["MesBufferHandleReset","MesBufferHandleReset function [RPC]","_rpc_mesbufferhandlereset","midles/MesBufferHandleReset","rpc.mesbufferhandlereset"]
old-location: rpc\mesbufferhandlereset.htm
tech.root: Rpc
ms.assetid: adc9681f-267e-4f6f-88a3-ec913e886dd1
ms.date: 12/05/2018
ms.keywords: MesBufferHandleReset, MesBufferHandleReset function [RPC], _rpc_mesbufferhandlereset, midles/MesBufferHandleReset, rpc.mesbufferhandlereset
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
 - MesBufferHandleReset
 - midles/MesBufferHandleReset
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
 - MesBufferHandleReset
---

# MesBufferHandleReset function


## -description

The 
<b>MesBufferHandleReset</b> function re-initializes the handle for buffer serialization.

## -parameters

### -param Handle

Handle to be initialized.

### -param HandleStyle

Style of <i>Handle</i>. Valid styles are <b>MES_FIXED_BUFFER_HANDLE</b> or <b>MES_DYNAMIC_BUFFER_HANDLE</b>.

### -param Operation

Operation code. Valid codes are <b>MES_ENCODE</b>, <b>MES_ENCODE_NDR64</b>, or <b>MES_DECODE</b>.

### -param pBuffer

For <b>MES_DECODE</b>, pointer to a pointer to the buffer containing the data to be decoded. 




For <b>MES_ENCODE</b>, pointer to a pointer to the buffer for 
<a href="/windows/desktop/Rpc/fixed-buffer-serialization">fixed buffer style</a>, and pointer to a pointer to return the buffer address for 
<a href="/windows/desktop/Rpc/dynamic-buffer-serialization">dynamic buffer style of serialization</a>.

For <b>MES_ENCODE_NDR64</b>, pointer to a pointer to the buffer for fixed buffer style, and pointer to a pointer to return the buffer address for dynamic buffer style of serialization, but explicitly uses NDR64 to encode the buffer. The user-provided buffer must be aligned to 16.

### -param BufferSize

Bytes of data to be decoded in the buffer. Note that this is used only for the fixed buffer style of serialization.

### -param pEncodedSize

Pointer to the size of the completed encoding. Note that this is used only when the operation is <b>MES_ENCODE</b> or <b>MES_ENCODE_NDR64</b>.

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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>MesBufferHandleReset</b> routine is used by applications to re-initialize a buffer style handle and save memory allocations.

## -see-also

<a href="/windows/desktop/api/midles/nf-midles-mesencodedynbufferhandlecreate">MesEncodeDynBufferHandleCreate</a>



<a href="/windows/desktop/api/midles/nf-midles-mesencodefixedbufferhandlecreate">MesEncodeFixedBufferHandleCreate</a>



<a href="/windows/desktop/api/midles/nf-midles-meshandlefree">MesHandleFree</a>