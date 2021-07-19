---
UID: NS:presentation.IPresentationSurfaceVtbl
tech.root: composition_presentation
title: IPresentationSurfaceVtbl
ms.date: 06/08/2021
targetos: Windows
description: Represents a v-table of pointers to `IPresentationSurface` functions.
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
req.typenames: IPresentationSurfaceVtbl
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - IPresentationSurfaceVtbl
f1_keywords:
 - IPresentationSurfaceVtbl
 - presentation/IPresentationSurfaceVtbl
dev_langs:
 - c++
---

## -description

Represents a v-table of pointers to `IPresentationSurface` functions.

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

### -field SetBuffer

Sets the presentation buffer associated with this presentation surface.

### -field SetColorSpace

Sets the type of color space used by the presentation surface.

### -field SetAlphaMode

Sets the transparency behavior of the presentation surface.

### -field SetSourceRect

Sets the area of the source presentation buffer to sample from.

### -field SetTransform

Sets the transform applied to the source buffer area to define the on-screen area where the buffer will appear.

### -field RestrictToOutput

Restricts presentation to a specific display adapter output.

### -field SetDisableReadback

Sets a flag to disable or enable buffer read back.

### -field SetLetterboxingMargins

Sets the size, in visual space, taken by each letterbox area.

## -remarks

## -see-also

[IPresentationSurface](nn-presentation-ipresentationsurface.md), [IUnknown interface](/windows/win32/api/unknwn/nn-unknwn-iunknown)
