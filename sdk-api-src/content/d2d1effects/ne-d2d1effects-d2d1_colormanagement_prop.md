---
UID: NE:d2d1effects.D2D1_COLORMANAGEMENT_PROP
title: D2D1_COLORMANAGEMENT_PROP (d2d1effects.h)
description: Identifiers for the properties of the Color management effect.
helpviewer_keywords: ["D2D1_COLORMANAGEMENT_PROP","D2D1_COLORMANAGEMENT_PROP enumeration [Direct2D]","D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE","D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT","D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT","D2D1_COLORMANAGEMENT_PROP_QUALITY","D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT","D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT","d2d1effects/D2D1_COLORMANAGEMENT_PROP","d2d1effects/D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE","d2d1effects/D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT","d2d1effects/D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT","d2d1effects/D2D1_COLORMANAGEMENT_PROP_QUALITY","d2d1effects/D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT","d2d1effects/D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT","direct2d.d2d1_colormanagement_prop"]
old-location: direct2d\d2d1_colormanagement_prop.htm
tech.root: Direct2D
ms.assetid: 1003B981-5F12-4CE9-B4A5-2E96CAEE6AC8
ms.date: 12/05/2018
ms.keywords: D2D1_COLORMANAGEMENT_PROP, D2D1_COLORMANAGEMENT_PROP enumeration [Direct2D], D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE, D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT, D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT, D2D1_COLORMANAGEMENT_PROP_QUALITY, D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT, D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT, d2d1effects/D2D1_COLORMANAGEMENT_PROP, d2d1effects/D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE, d2d1effects/D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT, d2d1effects/D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT, d2d1effects/D2D1_COLORMANAGEMENT_PROP_QUALITY, d2d1effects/D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT, d2d1effects/D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT, direct2d.d2d1_colormanagement_prop
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
req.typenames: D2D1_COLORMANAGEMENT_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_COLORMANAGEMENT_PROP
 - d2d1effects/D2D1_COLORMANAGEMENT_PROP
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
 - D2D1_COLORMANAGEMENT_PROP
---

# D2D1_COLORMANAGEMENT_PROP enumeration


## -description

Identifiers for the properties of the <a href="/windows/desktop/Direct2D/color-management">Color management effect</a>.

## -enum-fields

### -field D2D1_COLORMANAGEMENT_PROP_SOURCE_COLOR_CONTEXT:0

The source color space information. 
          

The type is <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>.

The default value is NULL.

### -field D2D1_COLORMANAGEMENT_PROP_SOURCE_RENDERING_INTENT:1

Which ICC rendering intent to use. 
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_colormanagement_rendering_intent">D2D1_COLORMANAGEMENT_RENDERING_INTENT</a>.

The default value is D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL.

### -field D2D1_COLORMANAGEMENT_PROP_DESTINATION_COLOR_CONTEXT:2

The destination color space information. 
          

The type is <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>.

The default value is NULL.

### -field D2D1_COLORMANAGEMENT_PROP_DESTINATION_RENDERING_INTENT:3

Which ICC rendering intent to use. 
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_colormanagement_rendering_intent">D2D1_COLORMANAGEMENT_RENDERING_INTENT</a>.

The default value is D2D1_COLORMANAGEMENT_RENDERING_INTENT_PERCEPTUAL.

### -field D2D1_COLORMANAGEMENT_PROP_ALPHA_MODE:4

How to interpret alpha data that is contained in the input image. 
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_colormanagement_alpha_mode">D2D1_COLORMANAGEMENT_ALPHA_MODE</a>.

The default value is D2D1_COLORMANAGEMENT_ALPHA_MODE_PREMULTIPLIED.

### -field D2D1_COLORMANAGEMENT_PROP_QUALITY:5

The quality level of the transform. 
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_colormanagement_quality">D2D1_COLORMANAGEMENT_QUALITY</a>.

The default value is D2D1_COLORMANAGEMENT_QUALITY_NORMAL.

### -field D2D1_COLORMANAGEMENT_PROP_FORCE_DWORD:0xffffffff
