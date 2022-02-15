---
UID: NE:d2d1effects.D2D1_BRIGHTNESS_PROP
title: D2D1_BRIGHTNESS_PROP (d2d1effects.h)
description: Identifiers for the properties of the Brightness effect.
helpviewer_keywords: ["D2D1_BRIGHTNESS_PROP","D2D1_BRIGHTNESS_PROP enumeration [Direct2D]","D2D1_BRIGHTNESS_PROP_BLACK_POINT","D2D1_BRIGHTNESS_PROP_WHITE_POINT","d2d1effects/D2D1_BRIGHTNESS_PROP","d2d1effects/D2D1_BRIGHTNESS_PROP_BLACK_POINT","d2d1effects/D2D1_BRIGHTNESS_PROP_WHITE_POINT","direct2d.d2d1_brightness_prop"]
old-location: direct2d\d2d1_brightness_prop.htm
tech.root: Direct2D
ms.assetid: 7D3CEF7A-AF72-451B-8E6A-A9DF8E85EDE9
ms.date: 12/05/2018
ms.keywords: D2D1_BRIGHTNESS_PROP, D2D1_BRIGHTNESS_PROP enumeration [Direct2D], D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1_BRIGHTNESS_PROP_WHITE_POINT, d2d1effects/D2D1_BRIGHTNESS_PROP, d2d1effects/D2D1_BRIGHTNESS_PROP_BLACK_POINT, d2d1effects/D2D1_BRIGHTNESS_PROP_WHITE_POINT, direct2d.d2d1_brightness_prop
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
req.typenames: D2D1_BRIGHTNESS_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BRIGHTNESS_PROP
 - d2d1effects/D2D1_BRIGHTNESS_PROP
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
 - D2D1_BRIGHTNESS_PROP
---

# D2D1_BRIGHTNESS_PROP enumeration


## -description

Identifiers for the properties of the <a href="/windows/desktop/Direct2D/brightness">Brightness effect</a>.

## -enum-fields

### -field D2D1_BRIGHTNESS_PROP_WHITE_POINT:0

The upper portion of the brightness transfer curve. The white point adjusts the appearance of the brighter portions of the image. 
          This property is for both the x value and the y value, in that order. Each of the values of this property are between 0 and 1, inclusive.
          

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>.

The default value is (1.0f, 1.0f).

### -field D2D1_BRIGHTNESS_PROP_BLACK_POINT:1

The lower portion of the brightness transfer curve. The black point adjusts the appearance of the darker portions of the image. 
          This property is for both the x value and the y value, in that order. Each of the values of this property are between 0 and 1, inclusive.
          

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>.

The default value is (0.0f, 0.0f).

### -field D2D1_BRIGHTNESS_PROP_FORCE_DWORD:0xffffffff
