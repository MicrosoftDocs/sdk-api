---
UID: NF:rpcdce.UuidHash
title: UuidHash function (rpcdce.h)
description: An application calls the UuidHash function to generate a hash value for a specified UUID.
helpviewer_keywords: ["UuidHash","UuidHash function [RPC]","_rpc_uuidhash","rpc.uuidhash","rpcdce/UuidHash"]
old-location: rpc\uuidhash.htm
tech.root: Rpc
ms.assetid: e96fafa6-1c10-42c1-8d85-5e338899411d
ms.date: 12/05/2018
ms.keywords: UuidHash, UuidHash function [RPC], _rpc_uuidhash, rpc.uuidhash, rpcdce/UuidHash
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
 - UuidHash
 - rpcdce/UuidHash
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
 - UuidHash
---

# UuidHash function


## -description

An application calls the 
<b>UuidHash</b> function to generate a hash value for a specified <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.

## -parameters

### -param Uuid

<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> for which a hash value is created.

### -param Status

Returns RPC_S_OK.

## -returns

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

An application calls 
<b>UuidHash</b> to generate a hash value for a specified <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>. The hash value returned is implementation dependent and may vary from implementation to implementation.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>