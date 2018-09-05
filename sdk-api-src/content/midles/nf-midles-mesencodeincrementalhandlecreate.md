---
UID: NF:midles.MesEncodeIncrementalHandleCreate
title: MesEncodeIncrementalHandleCreate function
author: windows-sdk-content
description: The MesEncodeIncrementalHandleCreate function creates an encoding and then initializes it for the incremental style of serialization.
old-location: rpc\mesencodeincrementalhandlecreate.htm
old-project: Rpc
ms.assetid: 54bbe560-08a9-4e41-9121-37aab0c209a9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MesEncodeIncrementalHandleCreate, MesEncodeIncrementalHandleCreate function [RPC], _rpc_mesencodeincrementalhandlecreate, midles/MesEncodeIncrementalHandleCreate, rpc.mesencodeincrementalhandlecreate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: midles.h
req.include-header: Rpc.h
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - MesEncodeIncrementalHandleCreate
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: GDI+ 1.1
---

# MesEncodeIncrementalHandleCreate function


## -description


The 
<b>MesEncodeIncrementalHandleCreate</b> function creates an encoding and then initializes it for the incremental style of serialization.


## -parameters




### -param UserState

Pointer to the user-supplied state object that coordinates the user-supplied <b>Alloc</b>, <b>Write</b>, and <b>Read</b> functions.


### -param AllocFn

Pointer to the user-supplied <b>Alloc</b> function.


### -param WriteFn

Pointer to the user-supplied <b>Write</b> function.


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>MesEncodeIncrementalHandleCreate</b> function is used by applications to create and initialize the handle for the incremental style of encoding or decoding. When using the incremental style of encoding, the user supplies an <b>Alloc</b> function to provide an empty buffer into which the encoded data is placed, and a <b>Write</b> function to call when the buffer is full or the encoding is complete. For additional information on the user-supplied <b>Alloc</b>, <b>Write</b>, and <b>Read</b> functions, see 
<a href="https://msdn.microsoft.com/36d6ea16-7d01-436e-ac32-610c3ddb8b8d">Serialization Services</a>.

When a stub is compiled using <b>-protocol all</b> or <b>-protocol ndr64</b> and the buffer is to be encoded using the NDR64 transfer syntax, the 
<a href="https://msdn.microsoft.com/adc9681f-267e-4f6f-88a3-ec913e886dd1">MesIncrementalHandleReset</a> function must be called with its <i>OpCode</i> parameter set to MES_ENCODE_NDR64.




## -see-also




<a href="https://msdn.microsoft.com/c7383b4d-94d1-4edd-ac29-c11fb5343156">Alloc</a>



<a href="https://msdn.microsoft.com/adc9681f-267e-4f6f-88a3-ec913e886dd1">MesBufferHandleReset</a>



<a href="https://msdn.microsoft.com/d4a4ac59-56fb-4693-9007-f358105f82f0">MesHandleFree</a>



<a href="https://msdn.microsoft.com/13ca3bd0-0527-4d54-84a1-aa6efca88e8d">MesIncrementalHandleReset</a>
 

 

