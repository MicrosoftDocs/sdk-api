---
UID: NE:d2d1effects.D2D1_SATURATION_PROP
title: D2D1_SATURATION_PROP (d2d1effects.h)
description: Identifiers for properties of the Saturation effect.
helpviewer_keywords: ["D2D1_SATURATION_PROP","D2D1_SATURATION_PROP enumeration [Direct2D]","D2D1_SATURATION_PROP_SATURATION","d2d1effects/D2D1_SATURATION_PROP","d2d1effects/D2D1_SATURATION_PROP_SATURATION","direct2d.d2d1_saturation_prop"]
old-location: direct2d\d2d1_saturation_prop.htm
tech.root: Direct2D
ms.assetid: 69F237FD-F9EE-4C6B-B6E1-673FE815FC6D
ms.date: 12/05/2018
ms.keywords: D2D1_SATURATION_PROP, D2D1_SATURATION_PROP enumeration [Direct2D], D2D1_SATURATION_PROP_SATURATION, d2d1effects/D2D1_SATURATION_PROP, d2d1effects/D2D1_SATURATION_PROP_SATURATION, direct2d.d2d1_saturation_prop
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
req.typenames: D2D1_SATURATION_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SATURATION_PROP
 - d2d1effects/D2D1_SATURATION_PROP
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
 - D2D1_SATURATION_PROP
---

# D2D1_SATURATION_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/saturation">Saturation effect</a>.

## -enum-fields

### -field D2D1_SATURATION_PROP_SATURATION:0

The saturation of the image. You can set the saturation to a value between 0 and 1. If you set it to 1 the output image is fully saturated. 
          If you set it to 0 the output image is monochrome. The saturation value is unitless.
          

The type is FLOAT.

The default is 0.5f.

### -field D2D1_SATURATION_PROP_FORCE_DWORD:0xffffffff
