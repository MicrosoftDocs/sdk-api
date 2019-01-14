---
UID: NF:rpcdce.UuidToStringW
title: UuidToStringW function
author: windows-sdk-content
description: The UuidToString function converts a UUID to a string.
old-location: rpc\uuidtostring.htm
tech.root: Rpc
ms.assetid: 49235b28-a0c5-4f69-9932-85350d7bcbb8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UuidToString, UuidToString function [RPC], UuidToStringA, UuidToStringW, _rpc_uuidtostring, rpc.uuidtostring, rpcdce/UuidToString, rpcdce/UuidToStringA, rpcdce/UuidToStringW
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UuidToStringW (Unicode) and UuidToStringA (ANSI)
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
 - UuidToString
 - UuidToStringA
 - UuidToStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UuidToStringW function


## -description


The 
<b>UuidToString</b> function converts a <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> to a string.


## -parameters




### -param Uuid [in]

Pointer to a binary 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.


### -param StringUuid [out]

Pointer to the null-terminated string into which the <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> specified in the <i>Uuid</i> parameter will be placed.


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
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls 
<b>UuidToString</b> to convert a binary <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> to a string <b>UUID</b>. The RPC run-time library allocates memory for the string returned in the <i>StringUuid</i> parameter. The application is responsible for calling 
<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> to deallocate that memory.




## -see-also




<a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a>



<a href="https://msdn.microsoft.com/90b3cf6b-a15b-4f91-9ba2-0e43fe3374df">UuidFromString</a>
 

 

