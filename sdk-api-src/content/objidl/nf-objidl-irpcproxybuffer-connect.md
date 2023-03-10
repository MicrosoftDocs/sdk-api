---
UID: NF:objidl.IRpcProxyBuffer.Connect
title: IRpcProxyBuffer::Connect (objidl.h)
description: The IRpcProxyBuffer::Connect method (objidl.h) initializes a client proxy, binding it to the specified RPC channel.
helpviewer_keywords: ["Connect","Connect method [COM]","Connect method [COM]","IRpcProxyBuffer interface","IRpcProxyBuffer interface [COM]","Connect method","IRpcProxyBuffer.Connect","IRpcProxyBuffer::Connect","_com_irpcproxybuffer_connect","com.irpcproxybuffer_connect","objidlbase/IRpcProxyBuffer::Connect"]
old-location: com\irpcproxybuffer_connect.htm
tech.root: com
ms.assetid: 18651110-9d20-4acc-b21e-9a93099e31bd
ms.date: 08/15/2022
ms.keywords: Connect, Connect method [COM], Connect method [COM],IRpcProxyBuffer interface, IRpcProxyBuffer interface [COM],Connect method, IRpcProxyBuffer.Connect, IRpcProxyBuffer::Connect, _com_irpcproxybuffer_connect, com.irpcproxybuffer_connect, objidlbase/IRpcProxyBuffer::Connect
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRpcProxyBuffer::Connect
 - objidl/IRpcProxyBuffer::Connect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IRpcProxyBuffer.Connect
---

# IRpcProxyBuffer::Connect


## -description

Initializes a client proxy, binding it to the specified RPC channel.

## -parameters

### -param pRpcChannelBuffer [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a> interface that the proxy uses to marshal data.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcproxybuffer">IRpcProxyBuffer</a>
