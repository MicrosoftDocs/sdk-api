---
UID: NF:objidl.IRpcStubBuffer.DebugServerRelease
title: IRpcStubBuffer::DebugServerRelease (objidl.h)
description: The IRpcStubBuffer::DebugServerRelease method (objidl.h) releases an interface pointer that was previously returned by DebugServerQueryInterface.
helpviewer_keywords: ["DebugServerRelease","DebugServerRelease method [COM]","DebugServerRelease method [COM]","IRpcStubBuffer interface","IRpcStubBuffer interface [COM]","DebugServerRelease method","IRpcStubBuffer.DebugServerRelease","IRpcStubBuffer::DebugServerRelease","_com_irpcstubbuffer_debugserverrelease","com.irpcstubbuffer_debugserverrelease","objidlbase/IRpcStubBuffer::DebugServerRelease"]
old-location: com\irpcstubbuffer_debugserverrelease.htm
tech.root: com
ms.assetid: 511f6e55-fb1d-4500-80fd-83e3fe2779d1
ms.date: 08/15/2022
ms.keywords: DebugServerRelease, DebugServerRelease method [COM], DebugServerRelease method [COM],IRpcStubBuffer interface, IRpcStubBuffer interface [COM],DebugServerRelease method, IRpcStubBuffer.DebugServerRelease, IRpcStubBuffer::DebugServerRelease, _com_irpcstubbuffer_debugserverrelease, com.irpcstubbuffer_debugserverrelease, objidlbase/IRpcStubBuffer::DebugServerRelease
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
 - IRpcStubBuffer::DebugServerRelease
 - objidl/IRpcStubBuffer::DebugServerRelease
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
 - IRpcStubBuffer.DebugServerRelease
---

# IRpcStubBuffer::DebugServerRelease


## -description

Releases an interface pointer that was previously returned by <a href="/windows/desktop/api/objidl/nf-objidl-irpcstubbuffer-debugserverqueryinterface">DebugServerQueryInterface</a>.

## -parameters

### -param pv [in]

A pointer to the interface that the caller no longer needs.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcstubbuffer">IRpcStubBuffer</a>
