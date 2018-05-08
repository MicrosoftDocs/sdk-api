---
UID: NF:midles.MesHandleFree
title: MesHandleFree function
author: windows-driver-content
description: The MesHandleFree function frees the memory allocated by the serialization handle.
old-location: rpc\meshandlefree.htm
old-project: Rpc
ms.assetid: d4a4ac59-56fb-4693-9007-f358105f82f0
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: MesHandleFree, MesHandleFree function [RPC], _rpc_meshandlefree, midles/MesHandleFree, rpc.meshandlefree
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	MesHandleFree
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>MesHandleFree</b> routine is used by applications to free the resources of the handle after encoding or decoding data.




## -see-also




<a href="https://msdn.microsoft.com/10a2312d-5969-4dde-bf62-308ad425569b">MesDecodeBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/4d8cb8e3-aa5a-4354-87e7-57543baa57e8">MesEncodeDynBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/7700e0f6-0f30-415c-9873-983ec6c249b2">MesEncodeFixedBufferHandleCreate</a>



<a href="https://msdn.microsoft.com/54bbe560-08a9-4e41-9121-37aab0c209a9">MesEncodeIncrementalHandleCreate</a>
 

 

