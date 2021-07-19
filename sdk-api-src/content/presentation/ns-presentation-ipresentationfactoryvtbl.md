---
UID: NS:presentation.IPresentationFactoryVtbl
tech.root: composition_presentation
title: IPresentationFactoryVtbl
ms.date: 06/08/2021
targetos: Windows
description: Represents a v-table of pointers to `IPresentationFactory` functions.
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
req.typenames: IPresentationFactoryVtbl
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - IPresentationFactoryVtbl
f1_keywords:
 - IPresentationFactoryVtbl
 - presentation/IPresentationFactoryVtbl
dev_langs:
 - c++
---

## -description

Represents a v-table of pointers to `IPresentationFactory` functions.

## -struct-fields

### -field b

### -field QueryInterface

Queries a COM object for a pointer to one of its interfaces.

### -field AddRef

Increments the reference count for an interface pointer to a COM object.

### -field Release

Decrements the reference count for an interface on a COM object.

### -field IsPresentationSupported

Gets a value that indicates whether presentation of any sort (with or without independent flip) is supported on the backing D3D device.

### -field IsPresentationSupportedWithIndependentFlip

Gets a value that indicates whether independent-flip-enabled presentation is supported on the backing D3D device.

### -field CreatePresentationManager

Creates a presentation manager.

## -remarks

## -see-also

[IPresentationFactory](nn-presentation-ipresentationfactory.md), [IUnknown interface](/windows/win32/api/unknwn/nn-unknwn-iunknown)
