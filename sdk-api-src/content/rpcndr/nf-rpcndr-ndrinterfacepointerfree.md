---
UID: NF:rpcndr.NdrInterfacePointerFree
title: NdrInterfacePointerFree function (rpcndr.h)
description: The NdrInterfacePointerFree function releases the interface pointer.
helpviewer_keywords: ["NdrInterfacePointerFree","NdrInterfacePointerFree function [RPC]","rpc.ndrinterfacepointerfree","rpcndr/NdrInterfacePointerFree"]
old-location: rpc\ndrinterfacepointerfree.htm
tech.root: Rpc
ms.assetid: fc40b621-b823-4a14-bd72-eab6086ec998
ms.date: 12/05/2018
ms.keywords: NdrInterfacePointerFree, NdrInterfacePointerFree function [RPC], rpc.ndrinterfacepointerfree, rpcndr/NdrInterfacePointerFree
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
 - NdrInterfacePointerFree
 - rpcndr/NdrInterfacePointerFree
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
 - NdrInterfacePointerFree
---

# NdrInterfacePointerFree function


## -description

The <b>NdrInterfacePointerFree</b> function releases the interface pointer.

## -parameters

### -param pStubMsg

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. This structure is for internal use only and should not be modified.

### -param pMemory [in]

Pointer to the interface pointer to be released.

### -param pFormat [in]

Pointer to the format string description.