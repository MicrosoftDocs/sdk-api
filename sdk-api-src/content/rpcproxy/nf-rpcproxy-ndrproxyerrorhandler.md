---
UID: NF:rpcproxy.NdrProxyErrorHandler
title: NdrProxyErrorHandler function (rpcproxy.h)
description: The NdrProxyErrorHandler function maps an exception into an HRESULT, with RPC facility code.
helpviewer_keywords: ["NdrProxyErrorHandler","NdrProxyErrorHandler function [RPC]","rpc.ndrproxyerrorhandler","rpcproxy/NdrProxyErrorHandler"]
old-location: rpc\ndrproxyerrorhandler.htm
tech.root: Rpc
ms.assetid: d453ac8d-5bcb-4565-be95-17b8b45c8d98
ms.date: 12/05/2018
ms.keywords: NdrProxyErrorHandler, NdrProxyErrorHandler function [RPC], rpc.ndrproxyerrorhandler, rpcproxy/NdrProxyErrorHandler
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
 - NdrProxyErrorHandler
 - rpcproxy/NdrProxyErrorHandler
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
 - NdrProxyErrorHandler
---

# NdrProxyErrorHandler function


## -description

The <b>NdrProxyErrorHandler</b> function maps an exception into an HRESULT, with RPC facility code.

## -parameters

### -param dwExceptionCode [in]

Exception code to be mapped.

## -returns

Returns the HRESULT.

