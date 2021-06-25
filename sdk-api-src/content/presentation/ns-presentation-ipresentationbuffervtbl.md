---
UID: NS:presentation.IPresentationBufferVtbl
tech.root: composition_presentation
title: IPresentationBufferVtbl
ms.date: 06/08/2021
targetos: Windows
description: Represents a v-table of pointers to `IPresentationBuffer` functions.
prerelease: true
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: presentation.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: IPresentationBufferVtbl
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - IPresentationBufferVtbl
f1_keywords:
 - IPresentationBufferVtbl
 - presentation/IPresentationBufferVtbl
dev_langs:
 - c++
---

## -description

Represents a v-table of pointers to `IPresentationBuffer` functions.

## -struct-fields

### -field b

### -field QueryInterface

Queries a COM object for a pointer to one of its interfaces.

### -field AddRef

Increments the reference count for an interface pointer to a COM object.

### -field Release

Decrements the reference count for an interface on a COM object.

### -field GetAvailableEvent

Gets a handle to an event that signals when the buffer is available.

### -field IsAvailable

Gets a value that indicates whether or not this buffer is available for use by the producer.

## -remarks

## -see-also

[IPresentationBuffer](nn-presentation-ipresentationbuffer.md), [IUnknown interface](/windows/win32/api/unknwn/nn-unknwn-iunknown)
