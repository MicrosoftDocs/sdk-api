---
UID: NF:objidl.IRpcStubBuffer.Connect
title: IRpcStubBuffer::Connect (objidl.h)
description: The IRpcStubBuffer::Connect method (objidl.h) initializes a server stub, binding it to the specified interface.
helpviewer_keywords: ["Connect","Connect method [COM]","Connect method [COM]","IRpcStubBuffer interface","IRpcStubBuffer interface [COM]","Connect method","IRpcStubBuffer.Connect","IRpcStubBuffer::Connect","_com_irpcstubbuffer_connect","com.irpcstubbuffer_connect","objidlbase/IRpcStubBuffer::Connect"]
old-location: com\irpcstubbuffer_connect.htm
tech.root: com
ms.assetid: 0a452287-b674-4b51-9690-316beeab4482
ms.date: 08/15/2022
ms.keywords: Connect, Connect method [COM], Connect method [COM],IRpcStubBuffer interface, IRpcStubBuffer interface [COM],Connect method, IRpcStubBuffer.Connect, IRpcStubBuffer::Connect, _com_irpcstubbuffer_connect, com.irpcstubbuffer_connect, objidlbase/IRpcStubBuffer::Connect
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
 - IRpcStubBuffer::Connect
 - objidl/IRpcStubBuffer::Connect
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
 - IRpcStubBuffer.Connect
---

# IRpcStubBuffer::Connect


## -description

Initializes a server stub, binding it to the specified interface.

## -parameters

### -param pUnkServer [in]

A pointer to the interface.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>
