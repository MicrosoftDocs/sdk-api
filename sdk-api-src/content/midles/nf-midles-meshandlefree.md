---
UID: NF:midles.MesHandleFree
title: MesHandleFree function (midles.h)
author: windows-sdk-content
description: The MesHandleFree function frees the memory allocated by the serialization handle.
old-location: rpc\meshandlefree.htm
tech.root: Rpc
ms.assetid: d4a4ac59-56fb-4693-9007-f358105f82f0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MesHandleFree, MesHandleFree function [RPC], _rpc_meshandlefree, midles/MesHandleFree, rpc.meshandlefree
ms.topic: function
f1_keywords: ["midles/MesHandleFree"]
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
 - MesHandleFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MesHandleFree function


## -description


The 
<b>MesHandleFree</b> function frees the memory allocated by the serialization handle.


## -parameters




### -param Handle

Handle to be freed.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>MesHandleFree</b> routine is used by applications to free the resources of the handle after encoding or decoding data.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/midles/nf-midles-mesdecodebufferhandlecreate">MesDecodeBufferHandleCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/midles/nf-midles-mesencodedynbufferhandlecreate">MesEncodeDynBufferHandleCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/midles/nf-midles-mesencodefixedbufferhandlecreate">MesEncodeFixedBufferHandleCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/midles/nf-midles-mesencodeincrementalhandlecreate">MesEncodeIncrementalHandleCreate</a>
 

 

