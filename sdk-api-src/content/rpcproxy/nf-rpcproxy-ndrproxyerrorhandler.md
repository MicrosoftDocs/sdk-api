---
UID: NF:rpcproxy.NdrProxyErrorHandler
title: NdrProxyErrorHandler function
author: windows-sdk-content
description: The NdrProxyErrorHandler function maps an exception into an HRESULT, with RPC facility code.
old-location: rpc\ndrproxyerrorhandler.htm
tech.root: Rpc
ms.assetid: d453ac8d-5bcb-4565-be95-17b8b45c8d98
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NdrProxyErrorHandler, NdrProxyErrorHandler function [RPC], rpc.ndrproxyerrorhandler, rpcproxy/NdrProxyErrorHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrProxyErrorHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrProxyErrorHandler function


## -description


The <b>NdrProxyErrorHandler</b> function maps an exception into an HRESULT, with RPC facility code.


## -parameters




### -param dwExceptionCode [in]

Exception code to be mapped.


## -returns



Returns the HRESULT.



