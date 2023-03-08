---
UID: NF:rpcndr.NdrClearOutParameters
title: NdrClearOutParameters function (rpcndr.h)
description: The NdrClearOutParameters function frees resources of the out parameter and clears its memory if the RPC call to the server fails.
helpviewer_keywords: ["NdrClearOutParameters","NdrClearOutParameters","NdrClearOutParameters function [RPC]","rpc.ndrclearoutparameters","rpcndr/NdrClearOutParameters"]
old-location: rpc\ndrclearoutparameters.htm
tech.root: Rpc
ms.assetid: f0ae23d5-3ec0-4e41-8c2c-5b6eb9bbb1b8
ms.date: 12/05/2018
ms.keywords: NdrClearOutParameters, NdrClearOutParameters, NdrClearOutParameters function [RPC], rpc.ndrclearoutparameters, rpcndr/NdrClearOutParameters
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
 - NdrClearOutParameters
 - rpcndr/NdrClearOutParameters
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
 - NdrClearOutParameters
---

# NdrClearOutParameters function


## -description

The <b>NdrClearOutParameters</b> function frees resources of the out parameter and clears its memory if the RPC call to the server fails.

## -parameters

### -param pStubMsg [in]

Pointer to <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The structure is for internal use only and should not be modified.

### -param pFormat [in]

Pointer to the format string description.

### -param ArgAddr [in, out]

Pointer to the out parameter to be freed.