---
UID: NE:d2d1effects.D2D1_ATLAS_PROP
title: D2D1_ATLAS_PROP (d2d1effects.h)
description: Identifiers for properties of the Atlas effect.
helpviewer_keywords: ["D2D1_ATLAS_PROP","D2D1_ATLAS_PROP enumeration [Direct2D]","D2D1_ATLAS_PROP_INPUT_PADDING_RECT","D2D1_ATLAS_PROP_INPUT_RECT","d2d1effects/D2D1_ATLAS_PROP","d2d1effects/D2D1_ATLAS_PROP_INPUT_PADDING_RECT","d2d1effects/D2D1_ATLAS_PROP_INPUT_RECT","direct2d.d2d1_atlas_prop"]
old-location: direct2d\d2d1_atlas_prop.htm
tech.root: Direct2D
ms.assetid: 7450C113-F1F0-433C-928B-19B0FF21B69B
ms.date: 12/05/2018
ms.keywords: D2D1_ATLAS_PROP, D2D1_ATLAS_PROP enumeration [Direct2D], D2D1_ATLAS_PROP_INPUT_PADDING_RECT, D2D1_ATLAS_PROP_INPUT_RECT, d2d1effects/D2D1_ATLAS_PROP, d2d1effects/D2D1_ATLAS_PROP_INPUT_PADDING_RECT, d2d1effects/D2D1_ATLAS_PROP_INPUT_RECT, direct2d.d2d1_atlas_prop
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
req.typenames: D2D1_ATLAS_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_ATLAS_PROP
 - d2d1effects/D2D1_ATLAS_PROP
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
 - D2D1_ATLAS_PROP
---

# D2D1_ATLAS_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/atlas">Atlas effect</a>.

## -enum-fields

### -field D2D1_ATLAS_PROP_INPUT_RECT:0

The portion of the image passed to the next effect.
            Type is D2D1_VECTOR_4F.
            Default value is (-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX).

### -field D2D1_ATLAS_PROP_INPUT_PADDING_RECT:1

The maximum size sampled for the output rectangle.
            Type is D2D1_VECTOR_4F.
            Default value is (-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX).

### -field D2D1_ATLAS_PROP_FORCE_DWORD:0xffffffff
