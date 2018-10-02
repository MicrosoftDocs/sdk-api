---
UID: NF:rpcdce.UuidFromStringA
title: UuidFromStringA function
author: windows-sdk-content
description: The UuidFromString function converts a string to a UUID.
old-location: rpc\uuidfromstring.htm
tech.root: Rpc
ms.assetid: 90b3cf6b-a15b-4f91-9ba2-0e43fe3374df
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: UuidFromString, UuidFromString function [RPC], UuidFromStringA, UuidFromStringW, _rpc_uuidfromstring, rpc.uuidfromstring, rpcdce/UuidFromString, rpcdce/UuidFromStringA, rpcdce/UuidFromStringW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UuidFromStringW (Unicode) and UuidFromStringA (ANSI)
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
 - UuidFromString
 - UuidFromStringA
 - UuidFromStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UuidFromStringA function


## -description


The 
<b>UuidFromString</b> function converts a string to a <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.


## -parameters




### -param StringUuid

Pointer to a string representation of a 
<a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a>.


### -param Uuid

Returns a pointer to a <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> in binary form.


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
<dt><b>RPC_S_INVALID_STRING_UUID</b></dt>
</dl>
</td>
<td width="60%">
The string <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>UuidFromString</b> function to convert a string <a href="https://msdn.microsoft.com/14288352-43c3-4e4d-a3f1-e924a8261d2b">UUID</a> to a binary <b>UUID</b>.




## -see-also




<a href="https://msdn.microsoft.com/49235b28-a0c5-4f69-9932-85350d7bcbb8">UuidToString</a>
 

 

