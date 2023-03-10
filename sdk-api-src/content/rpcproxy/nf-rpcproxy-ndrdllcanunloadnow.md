---
UID: NF:rpcproxy.NdrDllCanUnloadNow
title: NdrDllCanUnloadNow function (rpcproxy.h)
description: The NdrDllCanUnloadNow function determines whether the DLL that implements the proxy and stub is still in use. If not, the caller can safely unload the DLL from memory.
helpviewer_keywords: ["NdrDllCanUnloadNow","NdrDllCanUnloadNow function [RPC]","rpc.ndrdllcanunloadnow","rpcproxy/NdrDllCanUnloadNow"]
old-location: rpc\ndrdllcanunloadnow.htm
tech.root: Rpc
ms.assetid: 25cc5909-87f7-4670-a123-69bb28d891a5
ms.date: 12/05/2018
ms.keywords: NdrDllCanUnloadNow, NdrDllCanUnloadNow function [RPC], rpc.ndrdllcanunloadnow, rpcproxy/NdrDllCanUnloadNow
req.header: rpcproxy.h
req.include-header: 
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
 - NdrDllCanUnloadNow
 - rpcproxy/NdrDllCanUnloadNow
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
 - NdrDllCanUnloadNow
---

# NdrDllCanUnloadNow function


## -description

The <b>NdrDllCanUnloadNow</b> function determines whether the DLL that implements the proxy and stub is still in use. If not, the caller can safely unload the DLL from memory.

## -parameters

### -param pPSFactoryBuffer [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ipsfactorybuffer">CStdPSFactoryBuffer</a> object. The pointer is contained in the global variable, gPFactory, defined in RpcProxy.h.

## -returns

Returns S_OK if the DLL can be unloaded. Otherwise, it returns S_FALSE if the DLL cannot be unloaded.