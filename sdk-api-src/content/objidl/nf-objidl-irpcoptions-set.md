---
UID: NF:objidl.IRpcOptions.Set
title: IRpcOptions::Set (objidl.h)
description: The IRpcOptions::Set method (objidl.h) sets the value of an RPC binding option property.
helpviewer_keywords: ["IRpcOptions interface [COM]","Set method","IRpcOptions.Set","IRpcOptions::Set","Set","Set method [COM]","Set method [COM]","IRpcOptions interface","_com_irpcoptions_set","com.irpcoptions_set","objidlbase/IRpcOptions::Set"]
old-location: com\irpcoptions_set.htm
tech.root: com
ms.assetid: b4412e45-adc7-47e4-a19c-9ada6407e6dc
ms.date: 08/15/2022
ms.keywords: IRpcOptions interface [COM],Set method, IRpcOptions.Set, IRpcOptions::Set, Set, Set method [COM], Set method [COM],IRpcOptions interface, _com_irpcoptions_set, com.irpcoptions_set, objidlbase/IRpcOptions::Set
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
 - IRpcOptions::Set
 - objidl/IRpcOptions::Set
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
 - IRpcOptions.Set
---

# IRpcOptions::Set


## -description

Sets the value of an RPC binding option property.

## -parameters

### -param pPrx [in]

A pointer to the proxy whose property is being set.

### -param dwProperty [in]

An identifier of the property to be set, which must be COMBND_RPCTIMEOUT.

### -param dwValue [in]

The new value of the property.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -remarks

See <a href="/windows/desktop/api/objidl/nn-objidl-irpcoptions">IRpcOptions</a> for a table of the possible values of the COMBND_RPCTIMEOUT property.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcoptions">IRpcOptions</a>
