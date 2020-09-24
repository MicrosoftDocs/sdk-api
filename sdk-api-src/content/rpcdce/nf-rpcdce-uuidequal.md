---
UID: NF:rpcdce.UuidEqual
title: UuidEqual function (rpcdce.h)
description: An application calls the UuidEqual function to compare two UUIDs and determine whether they are equal.
helpviewer_keywords: ["UuidEqual","UuidEqual function [RPC]","_rpc_uuidequal","rpc.uuidequal","rpcdce/UuidEqual"]
old-location: rpc\uuidequal.htm
tech.root: Rpc
ms.assetid: ff83c66c-1f1f-4582-a93b-d7bb5181deec
ms.date: 12/05/2018
ms.keywords: UuidEqual, UuidEqual function [RPC], _rpc_uuidequal, rpc.uuidequal, rpcdce/UuidEqual
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
 - UuidEqual
 - rpcdce/UuidEqual
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
 - UuidEqual
---

# UuidEqual function


## -description

An application calls the  
<b>UuidEqual</b> function to compare two <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>s and determine whether they are equal.

## -parameters

### -param Uuid1

Pointer to a 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>. This <b>UUID</b> is compared with the <b>UUID</b> specified in the <i>Uuid2</i> parameter.

### -param Uuid2

Pointer to a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>. This <b>UUID</b> is compared with the <b>UUID</b> specified in the <i>Uuid1</i> parameter.

### -param Status

Returns RPC_S_OK.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>Uuid1</i> parameter is equal to the <i>Uuid2</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>Uuid1</i> parameter is not equal to the <i>Uuid2</i> parameter.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>