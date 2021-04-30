---
UID: NF:rpcdce.UuidCreateNil
title: UuidCreateNil function (rpcdce.h)
description: The UuidCreateNil function creates a nil-valued UUID.
helpviewer_keywords: ["UuidCreateNil","UuidCreateNil function [RPC]","_rpc_uuidcreatenil","rpc.uuidcreatenil","rpcdce/UuidCreateNil"]
old-location: rpc\uuidcreatenil.htm
tech.root: Rpc
ms.assetid: ee955482-e786-4478-bbaa-7c574ab1ecc5
ms.date: 12/05/2018
ms.keywords: UuidCreateNil, UuidCreateNil function [RPC], _rpc_uuidcreatenil, rpc.uuidcreatenil, rpcdce/UuidCreateNil
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
 - UuidCreateNil
 - rpcdce/UuidCreateNil
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
 - UuidCreateNil
---

# UuidCreateNil function


## -description

The 
<b>UuidCreateNil</b> function creates a nil-valued <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.

## -parameters

### -param NilUuid

Returns a nil-valued 
<a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>.

## -returns

Returns RPC_S_OK.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidfromstring">UuidFromString</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring">UuidToString</a>