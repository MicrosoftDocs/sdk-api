---
UID: NF:rpcdce.UuidIsNil
title: UuidIsNil function (rpcdce.h)
description: An application calls the UuidIsNil function to determine whether the specified UUID is a nil-valued UUID.
helpviewer_keywords: ["UuidIsNil","UuidIsNil function [RPC]","_rpc_uuidisnil","rpc.uuidisnil","rpcdce/UuidIsNil"]
old-location: rpc\uuidisnil.htm
tech.root: Rpc
ms.assetid: 0b764eca-552b-4431-812b-93fa0c03179e
ms.date: 12/05/2018
ms.keywords: UuidIsNil, UuidIsNil function [RPC], _rpc_uuidisnil, rpc.uuidisnil, rpcdce/UuidIsNil
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UuidIsNil
 - rpcdce/UuidIsNil
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
 - UuidIsNil
---

# UuidIsNil function


## -description

An application calls the  
<b>UuidIsNil</b> function to determine whether the specified <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> is a nil-valued <b>UUID</b>.

## -parameters

### -param Uuid

<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> to test for nil value.

### -param Status

Returns RPC_S_OK.

## -returns

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

This function acts as though the application called 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreatenil">UuidCreateNil</a>, and then called the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidequal">UuidEqual</a> to compare the returned nil-value <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> to the <b>UUID</b> specified in the <i>Uuid</i> parameter.

Upon completion, one of the following values is returned.

<table>
<tr>
<th>Returned value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>The <i>Uuid</i> parameter is a nil-valued <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>The <i>Uuid</i> parameter is not a nil-valued <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.</td>
</tr>
</table>
 


<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>