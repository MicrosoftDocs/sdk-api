---
UID: NF:rpcdce.UuidToStringW
title: UuidToStringW function (rpcdce.h)
description: The UuidToStringW (Unicode) function (rpcdce.h) converts a UUID to a string. 
helpviewer_keywords: ["UuidToString", "UuidToString function [RPC]", "UuidToStringW", "_rpc_uuidtostring", "rpc.uuidtostring", "rpcdce/UuidToString", "rpcdce/UuidToStringW"]
old-location: rpc\uuidtostring.htm
tech.root: Rpc
ms.assetid: 49235b28-a0c5-4f69-9932-85350d7bcbb8
ms.date: 08/15/2022
ms.keywords: UuidToString, UuidToString function [RPC], UuidToStringA, UuidToStringW, _rpc_uuidtostring, rpc.uuidtostring, rpcdce/UuidToString, rpcdce/UuidToStringA, rpcdce/UuidToStringW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UuidToStringW
 - rpcdce/UuidToStringW
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
 - UuidToString
 - UuidToStringA
 - UuidToStringW
---

# UuidToStringW function


## -description

The 
<b>UuidToString</b> function converts a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> to a string.

## -parameters

### -param Uuid [in]

Pointer to a binary 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.

### -param StringUuid [out]

Pointer to the null-terminated string into which the <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> specified in the <i>Uuid</i> parameter will be placed.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls 
<b>UuidToString</b> to convert a binary <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> to a string <b>UUID</b>. The RPC run-time library allocates memory for the string returned in the <i>StringUuid</i> parameter. The application is responsible for calling 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a> to deallocate that memory.





> [!NOTE]
> The rpcdce.h header defines UuidToString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidfromstring">UuidFromString</a>
