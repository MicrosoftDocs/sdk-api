---
UID: NF:rpcndr.NdrConformantArrayUnmarshall
title: NdrConformantArrayUnmarshall function
author: windows-sdk-content
description: The NdrConformantArrayUnmarshall function unmarshals a conformant array.
old-location: rpc\ndrconformantarrayunmarshall.htm
old-project: Rpc
ms.assetid: 09acbea7-a835-4365-917f-4b12b2602bf0
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: NdrConformantArrayUnmarshall, NdrConformantArrayUnmarshall
, NdrConformantArrayUnmarshall function [RPC], rpc.ndrconformantarrayunmarshall, rpcndr/NdrConformantArrayUnmarshall
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RpcRT4.dll
api_name:
-	NdrConformantArrayUnmarshall
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrConformantArrayUnmarshall function


## -description


The <b>NdrConformantArrayUnmarshall</b> function unmarshals a conformant array.


## -parameters




### -param pStubMsg

TBD


### -param ppMemory [out]

Address to a pointer to the buffer where the conformant array is unmarshalled. If set to <b>null</b>, or if the <i>fMustAlloc</i> is set to <b>TRUE</b>, the stub will allocate the memory.


### -param pFormat [in]

Pointer to the format string description.


### -param fMustAlloc [in]

Flag that specifies whether the stub must allocate the memory into which the conformant array is to be marshalled. Specify <b>TRUE</b> if RPC must allocate <i>ppMemory</i>.


#### - NdrConformantArrayUnmarshall [in]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. This structure is for internal use only and should not be modified.


## -returns



Returns <b>null</b> upon success. If an error occurs, the function throws one of the following exception codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_BAD_STUB_DATA</b></dt>
</dl>
</td>
<td width="60%">
The network  is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_INVALID_BOUND</b></dt>
</dl>
</td>
<td width="60%">
The network  is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCESS_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
An access violation occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred in RPC.

</td>
</tr>
</table>
 




## -remarks



The <b>NdrConformantArrayUnmarshall</b> function is used by both the client- and server-side stub to unmarshall a conformant array. The stub might allocate memory as necessary. For example, pArray in the sample on this page points to a conformant array. 

<b>NdrConformantArrayUnmarshall</b> should only be called in the context of an RPC stub, after the client or server stub has been initialized.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void  ConfArray([in] long size,
        [in,size_is(size)] long *pArray);         // conformant array
</pre>
</td>
</tr>
</table></span></div>


