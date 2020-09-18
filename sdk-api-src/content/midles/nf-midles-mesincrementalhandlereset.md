---
UID: NF:midles.MesIncrementalHandleReset
title: MesIncrementalHandleReset function (midles.h)
description: The MesIncrementalHandleReset function re-initializes the handle for incremental serialization.
helpviewer_keywords: ["MesIncrementalHandleReset","MesIncrementalHandleReset function [RPC]","_rpc_mesincrementalhandlereset","midles/MesIncrementalHandleReset","rpc.mesincrementalhandlereset"]
old-location: rpc\mesincrementalhandlereset.htm
tech.root: Rpc
ms.assetid: 13ca3bd0-0527-4d54-84a1-aa6efca88e8d
ms.date: 12/05/2018
ms.keywords: MesIncrementalHandleReset, MesIncrementalHandleReset function [RPC], _rpc_mesincrementalhandlereset, midles/MesIncrementalHandleReset, rpc.mesincrementalhandlereset
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
 - MesIncrementalHandleReset
 - midles/MesIncrementalHandleReset
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
 - MesIncrementalHandleReset
---

# MesIncrementalHandleReset function


## -description

The 
<b>MesIncrementalHandleReset</b> function re-initializes the handle for incremental serialization.

## -parameters

### -param Handle

Handle to be re-initialized.

### -param UserState

Depending on the function, pointer to the user-supplied block that coordinates successive calls to the user-supplied <b>Alloc</b>, <b>Write</b>, and <b>Read</b> functions.

### -param AllocFn

Pointer to the user-supplied <b>Alloc</b> function. This parameter can be <b>NULL</b> if the operation does not require it, or if the handle was previously initiated with the pointer.

### -param WriteFn

Pointer to the user-supplied <b>Write</b> function. This parameter can be <b>NULL</b> if the operation does not require it, or if the handle was previously initiated with the pointer.

### -param ReadFn

Pointer to the user-supplied <b>Read</b> function. This parameter can be <b>NULL</b> if the operation does not require it, or if the handle was previously initiated with the pointer.

### -param Operation

Specifies the operation. Valid operations are <b>MES_ENCODE</b>, <b>MES_ENCODE_NDR64</b>, or <b>MES_DECODE</b>.

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
<b>MesIncrementalHandleReset</b> routine is used by applications to re-initialize the handle for the incremental style of encoding or decoding. For additional information on the user-supplied <b>Alloc</b>, <b>Write</b>, and <b>Read</b> functions, see 
<a href="/windows/desktop/Rpc/serialization-services">Serialization Services</a>.

## -see-also

<a href="/windows/desktop/Rpc/incremental-serialization">Alloc</a>



<a href="/windows/desktop/api/midles/nf-midles-mesbufferhandlereset">MesBufferhandleReset</a>



<a href="/windows/desktop/api/midles/nf-midles-mesencodeincrementalhandlecreate">MesEncodeIncrementalHandleCreate</a>



<a href="/windows/desktop/api/midles/nf-midles-meshandlefree">MesHandleFree</a>