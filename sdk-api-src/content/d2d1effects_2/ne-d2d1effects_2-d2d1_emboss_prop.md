---
UID: NE:d2d1effects_2.D2D1_EMBOSS_PROP
title: D2D1_EMBOSS_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Emboss effect.
helpviewer_keywords: ["D2D1_EMBOSS_PROP","D2D1_EMBOSS_PROP enumeration [Direct2D]","D2D1_EMBOSS_PROP_DIRECTION","D2D1_EMBOSS_PROP_HEIGHT","d2d1effects_2/D2D1_EMBOSS_PROP","d2d1effects_2/D2D1_EMBOSS_PROP_DIRECTION","d2d1effects_2/D2D1_EMBOSS_PROP_HEIGHT","direct2d.d2d1_emboss_prop"]
old-location: direct2d\d2d1_emboss_prop.htm
tech.root: Direct2D
ms.assetid: 1AC8F0FE-8D51-4DDD-94FB-DC7AC890C95F
ms.date: 12/05/2018
ms.keywords: D2D1_EMBOSS_PROP, D2D1_EMBOSS_PROP enumeration [Direct2D], D2D1_EMBOSS_PROP_DIRECTION, D2D1_EMBOSS_PROP_HEIGHT, d2d1effects_2/D2D1_EMBOSS_PROP, d2d1effects_2/D2D1_EMBOSS_PROP_DIRECTION, d2d1effects_2/D2D1_EMBOSS_PROP_HEIGHT, direct2d.d2d1_emboss_prop
req.header: d2d1effects_2.h
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
req.typenames: D2D1_EMBOSS_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_EMBOSS_PROP
 - d2d1effects_2/D2D1_EMBOSS_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_EMBOSS_PROP
---

# D2D1_EMBOSS_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/emboss-effect">Emboss effect</a>.

## -enum-fields

### -field D2D1_EMBOSS_PROP_HEIGHT:0

The D2D1_EMBOSS_PROP_HEIGHT property is a float value controlling the strength of the embossing effect.  The allowed range is 0.0 to 10.0.  The default value is 1.0.

### -field D2D1_EMBOSS_PROP_DIRECTION:1

The D2D1_EMBOSS_PROP_DIRECTION property is a float value specifying the light direction used to create the effect. The allowed range is 0.0 to 360.0.  The default value is 0.0.

### -field D2D1_EMBOSS_PROP_FORCE_DWORD:0xffffffff
