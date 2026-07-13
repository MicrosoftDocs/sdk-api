---
UID: NF:rpcdce.UuidFromStringW
title: UuidFromStringW function (rpcdce.h)
description: The UuidFromStringW (Unicode) function (rpcdce.h) converts a string to a UUID.
helpviewer_keywords: ["UuidFromString", "UuidFromString function [RPC]", "UuidFromStringW", "_rpc_uuidfromstring", "rpc.uuidfromstring", "rpcdce/UuidFromString", "rpcdce/UuidFromStringW"]
old-location: rpc\uuidfromstring.htm
tech.root: Rpc
ms.assetid: 90b3cf6b-a15b-4f91-9ba2-0e43fe3374df
ms.date: 08/15/2022
ms.keywords: UuidFromString, UuidFromString function [RPC], UuidFromStringA, UuidFromStringW, _rpc_uuidfromstring, rpc.uuidfromstring, rpcdce/UuidFromString, rpcdce/UuidFromStringA, rpcdce/UuidFromStringW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UuidFromStringW
 - rpcdce/UuidFromStringW
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
 - UuidFromString
 - UuidFromStringA
 - UuidFromStringW
---

# UuidFromStringW function


## -description

The 
<b>UuidFromString</b> function converts a string to a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.

## -parameters

### -param StringUuid

Pointer to a string representation of a 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.

### -param Uuid

Returns a pointer to a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> in binary form.

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
The string <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls the 
<b>UuidFromString</b> function to convert a string <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> to a binary <b>UUID</b>.





> [!NOTE]
> The rpcdce.h header defines UuidFromString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring">UuidToString</a>
