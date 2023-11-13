---
UID: NF:rpcdce.UuidToString
title: UuidToString function (rpcdce.h)
description: The UuidToString function (rpcdce.h) converts a UUID to a string.
helpviewer_keywords: ["UuidToString","UuidToString function [RPC]","UuidToStringA","UuidToStringW","_rpc_uuidtostring","rpc.uuidtostring","rpcdce/UuidToString","rpcdce/UuidToStringA","rpcdce/UuidToStringW"]
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
 - UuidToString
 - rpcdce/UuidToString
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

# UuidToString function


## -description

The 
<b>UuidToString</b> function converts a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> to a string.

## -parameters

### -param Uuid [in]

Pointer to a binary [UUID](/windows/win32/rpc/rpcdce/ns-rpcdce-uuid).

### -param StringUuid [out]

Pointer to the null-terminated string into which the <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> specified in the <i>Uuid</i> parameter will be placed.

The UUID format is **xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx**.

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

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcstringfree">RpcStringFree</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidfromstring">UuidFromString</a>
