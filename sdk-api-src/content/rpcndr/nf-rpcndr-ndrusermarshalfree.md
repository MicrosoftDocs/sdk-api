---
UID: NF:rpcndr.NdrUserMarshalFree
title: NdrUserMarshalFree function (rpcndr.h)
description: The NdrUserMarshalFree function frees the user marshal object.
helpviewer_keywords: ["NdrUserMarshalFree","NdrUserMarshalFree function [RPC]","rpc.ndrusermarshalfree","rpcndr/NdrUserMarshalFree"]
old-location: rpc\ndrusermarshalfree.htm
tech.root: Rpc
ms.assetid: 3b850938-13f3-4173-86bb-8b01ac0c5809
ms.date: 12/05/2018
ms.keywords: NdrUserMarshalFree, NdrUserMarshalFree function [RPC], rpc.ndrusermarshalfree, rpcndr/NdrUserMarshalFree
req.header: rpcndr.h
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
 - NdrUserMarshalFree
 - rpcndr/NdrUserMarshalFree
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
 - NdrUserMarshalFree
---

# NdrUserMarshalFree function


## -description

The <b>NdrUserMarshalFree</b> function frees the user marshal object.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.

### -param pMemory [in]

Pointer to be freed.

### -param pFormat [in]

Pointer's format string description.

## -remarks

You should never free the top level object, it is freed by the system.