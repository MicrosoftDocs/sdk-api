---
UID: NF:objidl.IRpcStubBuffer.Invoke
title: IRpcStubBuffer::Invoke (objidl.h)
description: The IRpcStubBuffer::Invoke method (objidl.h) invokes the interface that a stub represents.
helpviewer_keywords: ["IRpcStubBuffer interface [COM]","Invoke method","IRpcStubBuffer.Invoke","IRpcStubBuffer::Invoke","Invoke","Invoke method [COM]","Invoke method [COM]","IRpcStubBuffer interface","_com_irpcstubbuffer_invoke","com.irpcstubbuffer_invoke","objidlbase/IRpcStubBuffer::Invoke"]
old-location: com\irpcstubbuffer_invoke.htm
tech.root: com
ms.assetid: 78d20830-78d7-4395-aaec-8a86b7c41cc7
ms.date: 08/15/2022
ms.keywords: IRpcStubBuffer interface [COM],Invoke method, IRpcStubBuffer.Invoke, IRpcStubBuffer::Invoke, Invoke, Invoke method [COM], Invoke method [COM],IRpcStubBuffer interface, _com_irpcstubbuffer_invoke, com.irpcstubbuffer_invoke, objidlbase/IRpcStubBuffer::Invoke
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IRpcStubBuffer::Invoke
 - objidl/IRpcStubBuffer::Invoke
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
 - IRpcStubBuffer.Invoke
---

# IRpcStubBuffer::Invoke


## -description

Invokes the interface that a stub represents.

## -parameters

### -param _prpcmsg [in, out]

A pointer to an <a href="/windows/desktop/api/objidl/ns-objidl-rpcolemessage">RPCOLEMESSAGE</a> data structure containing the marshaled invocation arguments.

### -param _pRpcChannelBuffer [in]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a> interface that controls an RPC marshaling channel.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>
