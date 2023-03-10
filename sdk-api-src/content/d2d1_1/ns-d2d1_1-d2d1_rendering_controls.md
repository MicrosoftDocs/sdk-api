---
UID: NS:d2d1_1.D2D1_RENDERING_CONTROLS
title: D2D1_RENDERING_CONTROLS (d2d1_1.h)
description: Describes limitations to be applied to an imaging effect renderer.
helpviewer_keywords: ["D2D1_RENDERING_CONTROLS","D2D1_RENDERING_CONTROLS structure [Direct2D]","PD2D1_RENDERING_CONTROLS","PD2D1_RENDERING_CONTROLS structure pointer [Direct2D]","d2d1_1/D2D1_RENDERING_CONTROLS","d2d1_1/PD2D1_RENDERING_CONTROLS","direct2d.d2d1_rendering_controls"]
old-location: direct2d\d2d1_rendering_controls.htm
tech.root: Direct2D
ms.assetid: e563cbb0-2ee0-43d8-978c-0bde1950a926
ms.date: 12/05/2018
ms.keywords: D2D1_RENDERING_CONTROLS, D2D1_RENDERING_CONTROLS structure [Direct2D], PD2D1_RENDERING_CONTROLS, PD2D1_RENDERING_CONTROLS structure pointer [Direct2D], d2d1_1/D2D1_RENDERING_CONTROLS, d2d1_1/PD2D1_RENDERING_CONTROLS, direct2d.d2d1_rendering_controls
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_RENDERING_CONTROLS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_RENDERING_CONTROLS
 - d2d1_1/D2D1_RENDERING_CONTROLS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_RENDERING_CONTROLS
---

# D2D1_RENDERING_CONTROLS structure


## -description

Describes limitations to be applied to an imaging effect renderer.

## -struct-fields

### -field bufferPrecision

The buffer precision used by default if the buffer precision is not otherwise specified by the effect or by the transform.

### -field tileSize

The tile allocation size to be used by the imaging effect renderer.

## -remarks

The renderer can allocate tiles larger than the minimum tile allocation. The allocated tiles will be powers of two of the minimum size on each axis, except that the size on each axis will not exceed the guaranteed maximum texture size for the device feature level. 

The "minimum pixel render extent" is the size of the square tile below which the renderer will expand the tile allocation rather than attempting to subdivide the rendering tile any further. When this threshold is reached, the allocation tile size is expanded. This might occur repeatedly until either rendering can proceed, or it is determined that the graph can't be rendered.

The buffer precision is used for intermediate buffers if it is otherwise unspecified by the effects (for example, through calling [SetValue](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) on the effect with the [D2D1_PROPERTY_PRECISION](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property) property) or the internal effect topology if required. If the buffer type on the context is [D2D1_BUFFER_PRECISION_UNKNOWN](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision), and otherwise not specified by the effect or transform, then the precision of the output will be the maximum precision of the inputs to the transform. The buffer precision does not affect the number of channels used.

## -see-also

[ID2D1DeviceContext::SetRenderingControls method](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls_))

