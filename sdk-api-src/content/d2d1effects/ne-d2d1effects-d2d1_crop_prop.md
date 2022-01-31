---
UID: NE:d2d1effects.D2D1_CROP_PROP
title: D2D1_CROP_PROP (d2d1effects.h)
description: Identifiers for properties of the Crop effect.
helpviewer_keywords: ["D2D1_CROP_PROP","D2D1_CROP_PROP enumeration [Direct2D]","D2D1_CROP_PROP_BORDER_MODE","D2D1_CROP_PROP_RECT","d2d1effects/D2D1_CROP_PROP","d2d1effects/D2D1_CROP_PROP_BORDER_MODE","d2d1effects/D2D1_CROP_PROP_RECT","direct2d.d2d1_crop_prop"]
old-location: direct2d\d2d1_crop_prop.htm
tech.root: Direct2D
ms.assetid: E9C00E8A-AD1E-475C-9B81-A5EB995669C6
ms.date: 12/05/2018
ms.keywords: D2D1_CROP_PROP, D2D1_CROP_PROP enumeration [Direct2D], D2D1_CROP_PROP_BORDER_MODE, D2D1_CROP_PROP_RECT, d2d1effects/D2D1_CROP_PROP, d2d1effects/D2D1_CROP_PROP_BORDER_MODE, d2d1effects/D2D1_CROP_PROP_RECT, direct2d.d2d1_crop_prop
req.header: d2d1effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_CROP_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_CROP_PROP
 - d2d1effects/D2D1_CROP_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_CROP_PROP
---

# D2D1_CROP_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/crop">Crop effect</a>.

## -enum-fields

### -field D2D1_CROP_PROP_RECT:0

The region to be cropped specified as a vector in the form (left, top, width, height). Units are in DIPs.
            

<div class="alert"><b>Note</b>  The rectangle will be truncated if it overlaps the edge boundaries of the input image.</div>
<div> </div>
Type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f">D2D1_VECTOR_4F</a>


Default value is {-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}

### -field D2D1_CROP_PROP_BORDER_MODE:1

Indicates how the effect handles the crop rectangle falling on fractional pixel coordinates.
          

Type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_border_mode">D2D1_BORDER_MODE</a>.

Default value is D2D1_BORDER_MODE_SOFT.

### -field D2D1_CROP_PROP_FORCE_DWORD:0xffffffff
