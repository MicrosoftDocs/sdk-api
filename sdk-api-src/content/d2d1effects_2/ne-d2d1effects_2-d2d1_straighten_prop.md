---
UID: NE:d2d1effects_2.D2D1_STRAIGHTEN_PROP
title: D2D1_STRAIGHTEN_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Straighten effect.
helpviewer_keywords: ["D2D1_STRAIGHTEN_PROP","D2D1_STRAIGHTEN_PROP enumeration [Direct2D]","D2D1_STRAIGHTEN_PROP_ANGLE","D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE","D2D1_STRAIGHTEN_PROP_SCALE_MODE","d2d1effects_2/D2D1_STRAIGHTEN_PROP","d2d1effects_2/D2D1_STRAIGHTEN_PROP_ANGLE","d2d1effects_2/D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE","d2d1effects_2/D2D1_STRAIGHTEN_PROP_SCALE_MODE","direct2d.d2d1_straighten_prop"]
old-location: direct2d\d2d1_straighten_prop.htm
tech.root: Direct2D
ms.assetid: AD22B649-E4FE-41BD-85FE-B000CCB7F48D
ms.date: 12/05/2018
ms.keywords: D2D1_STRAIGHTEN_PROP, D2D1_STRAIGHTEN_PROP enumeration [Direct2D], D2D1_STRAIGHTEN_PROP_ANGLE, D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, D2D1_STRAIGHTEN_PROP_SCALE_MODE, d2d1effects_2/D2D1_STRAIGHTEN_PROP, d2d1effects_2/D2D1_STRAIGHTEN_PROP_ANGLE, d2d1effects_2/D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, d2d1effects_2/D2D1_STRAIGHTEN_PROP_SCALE_MODE, direct2d.d2d1_straighten_prop
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
req.typenames: D2D1_STRAIGHTEN_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_STRAIGHTEN_PROP
 - d2d1effects_2/D2D1_STRAIGHTEN_PROP
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
 - D2D1_STRAIGHTEN_PROP
---

# D2D1_STRAIGHTEN_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/straighten-effect">Straighten effect</a>.

## -enum-fields

### -field D2D1_STRAIGHTEN_PROP_ANGLE:0

The D2D1_STRAIGHTEN_PROP_ANGLE property is a float value that specifies how much the image should be rotated.  The allowed range is -45.0 to 45.0.  The default value is 0.0.

### -field D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE:1

The D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE property is a boolean value that specifies whether the image will be scaled such that the original size is maintained without any invalid regions.
          The default value is True.

### -field D2D1_STRAIGHTEN_PROP_SCALE_MODE:2

The D2D1_STRAIGHTEN_PROP_SCALE_MODE property is a <a href="/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_scale_mode">D2D1_STRAIGHTEN_SCALE_MODE</a> enumeration value indicating the scaling mode that should be used.

### -field D2D1_STRAIGHTEN_PROP_FORCE_DWORD:0xffffffff
