---
UID: NS:presentation.IPresentationContentVtbl
tech.root: composition_presentation
title: IPresentationContentVtbl
ms.date: 06/08/2021
targetos: Windows
description: Represents a v-table of pointers to `IPresentationContent` functions.
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
req.typenames: IPresentationContentVtbl
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - IPresentationContentVtbl
f1_keywords:
 - IPresentationContentVtbl
 - presentation/IPresentationContentVtbl
dev_langs:
 - c++
---

## -description

Represents a v-table of pointers to `IPresentationContent` functions.

## -struct-fields

### -field b

### -field QueryInterface

Queries a COM object for a pointer to one of its interfaces.

### -field AddRef

Increments the reference count for an interface pointer to a COM object.

### -field Release

Decrements the reference count for an interface on a COM object.

### -field SetTag

Sets a user-defined tag to associate with this content. This tag is how the content is referenced in statistics.

## -remarks

## -see-also

[IPresentationContent](nn-presentation-ipresentationcontent.md), [IUnknown interface](/windows/win32/api/unknwn/nn-unknwn-iunknown)
