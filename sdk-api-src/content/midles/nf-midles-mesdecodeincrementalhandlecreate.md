---
UID: NF:midles.MesDecodeIncrementalHandleCreate
title: MesDecodeIncrementalHandleCreate function (midles.h)
author: windows-sdk-content
description: The MesDecodeIncrementalHandleCreate function creates a decoding handle for the incremental style of serialization.
old-location: rpc\mesdecodeincrementalhandlecreate.htm
tech.root: Rpc
ms.assetid: 0fe051be-e5c0-44b2-8ebc-5aa362fe4008
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MesDecodeIncrementalHandleCreate, MesDecodeIncrementalHandleCreate function [RPC], _rpc_mesdecodeincrementalhandlecreate, midles/MesDecodeIncrementalHandleCreate, rpc.mesdecodeincrementalhandlecreate
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
 - MesDecodeIncrementalHandleCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MesDecodeIncrementalHandleCreate function


## -description


The 
<b>MesDecodeIncrementalHandleCreate</b> function creates a decoding handle for the incremental style of serialization.


## -parameters




### -param UserState

Pointer to the user-supplied state object that coordinates the user-supplied <b>Alloc</b>, <b>Write</b>, and <b>Read</b> functions.


### -param ReadFn

Pointer to the <b>Read</b> function.


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
<b>MesDecodeIncrementalHandleCreate</b> function is used by applications to create the handle and initialize it for the incremental style of decoding. When using the incremental style of decoding, the user supplies a <b>Read</b> function to provide a buffer containing the next part of the data to be decoded. The buffer must be aligned at 8, and the size of the buffer must be a multiple of 8. For additional information on the user-supplied <b>Alloc</b>, <b>Write</b>, and <b>Read</b> functions, see 
<a href="https://msdn.microsoft.com/36d6ea16-7d01-436e-ac32-610c3ddb8b8d">Serialization Services</a>.




## -see-also




<a href="https://msdn.microsoft.com/c7383b4d-94d1-4edd-ac29-c11fb5343156">Alloc</a>



<a href="https://msdn.microsoft.com/d4a4ac59-56fb-4693-9007-f358105f82f0">MesHandleFree</a>



<a href="https://msdn.microsoft.com/13ca3bd0-0527-4d54-84a1-aa6efca88e8d">MesIncrementalHandleReset</a>
 

 

