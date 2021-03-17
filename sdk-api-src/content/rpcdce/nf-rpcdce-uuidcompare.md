---
UID: NF:rpcdce.UuidCompare
title: UuidCompare function (rpcdce.h)
description: An application calls the UuidCompare function to compare two UUIDs and determine their order. The returned value gives the order.
helpviewer_keywords: ["UuidCompare","UuidCompare function [RPC]","_rpc_uuidcompare","rpc.uuidcompare","rpcdce/UuidCompare"]
old-location: rpc\uuidcompare.htm
tech.root: Rpc
ms.assetid: 9a8c558b-c438-45f7-ac0f-1da20eb26e29
ms.date: 12/05/2018
ms.keywords: UuidCompare, UuidCompare function [RPC], _rpc_uuidcompare, rpc.uuidcompare, rpcdce/UuidCompare
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
 - UuidCompare
 - rpcdce/UuidCompare
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
 - UuidCompare
---

# UuidCompare function


## -description

An application calls the  
<b>UuidCompare</b> function to compare two <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>s and determine their order. The returned value gives the order.

## -parameters

### -param Uuid1

Pointer to a 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>. This <b>UUID</b> is compared with the <b>UUID</b> specified in the <i>Uuid2</i> parameter.

### -param Uuid2

Pointer to a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>. This <b>UUID</b> is compared with the <b>UUID</b> specified in the <i>Uuid1</i> parameter.

### -param Status

Returns any errors that may occur, and will typically be set by the function to RPC_S_OK upon return.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>–1</b></dt>
</dl>
</td>
<td width="60%">
The <i>Uuid1</i> parameter is less than the <i>Uuid2</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The <i>Uuid1</i> parameter is equal to the <i>Uuid2</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
The <i>Uuid1</i> parameter is greater than the <i>Uuid2</i> parameter.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>