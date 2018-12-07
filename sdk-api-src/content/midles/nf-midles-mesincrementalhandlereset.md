---
UID: NF:midles.MesIncrementalHandleReset
title: MesIncrementalHandleReset function
author: windows-sdk-content
description: The MesIncrementalHandleReset function re-initializes the handle for incremental serialization.
old-location: rpc\mesincrementalhandlereset.htm
tech.root: rpc
ms.assetid: 13ca3bd0-0527-4d54-84a1-aa6efca88e8d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MesIncrementalHandleReset, MesIncrementalHandleReset function [RPC], _rpc_mesincrementalhandlereset, midles/MesIncrementalHandleReset, rpc.mesincrementalhandlereset
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
 - MesIncrementalHandleReset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>MesIncrementalHandleReset</b> routine is used by applications to re-initialize the handle for the incremental style of encoding or decoding. For additional information on the user-supplied <b>Alloc</b>, <b>Write</b>, and <b>Read</b> functions, see 
<a href="https://msdn.microsoft.com/36d6ea16-7d01-436e-ac32-610c3ddb8b8d">Serialization Services</a>.




## -see-also




<a href="https://msdn.microsoft.com/c7383b4d-94d1-4edd-ac29-c11fb5343156">Alloc</a>



<a href="https://msdn.microsoft.com/adc9681f-267e-4f6f-88a3-ec913e886dd1">MesBufferhandleReset</a>



<a href="https://msdn.microsoft.com/54bbe560-08a9-4e41-9121-37aab0c209a9">MesEncodeIncrementalHandleCreate</a>



<a href="https://msdn.microsoft.com/d4a4ac59-56fb-4693-9007-f358105f82f0">MesHandleFree</a>
 

 

