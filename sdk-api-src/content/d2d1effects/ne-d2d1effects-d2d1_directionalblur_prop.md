---
UID: NE:d2d1effects.D2D1_DIRECTIONALBLUR_PROP
title: D2D1_DIRECTIONALBLUR_PROP (d2d1effects.h)
description: Identifiers for properties of the Directional blur effect.
helpviewer_keywords: ["D2D1_DIRECTIONALBLUR_PROP","D2D1_DIRECTIONALBLUR_PROP enumeration [Direct2D]","D2D1_DIRECTIONALBLUR_PROP_ANGLE","D2D1_DIRECTIONALBLUR_PROP_BORDER_MODE","D2D1_DIRECTIONALBLUR_PROP_OPTIMIZATION","D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION","d2d1effects/D2D1_DIRECTIONALBLUR_PROP","d2d1effects/D2D1_DIRECTIONALBLUR_PROP_ANGLE","d2d1effects/D2D1_DIRECTIONALBLUR_PROP_BORDER_MODE","d2d1effects/D2D1_DIRECTIONALBLUR_PROP_OPTIMIZATION","d2d1effects/D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION","direct2d.d2d1_directionalblur_prop"]
old-location: direct2d\d2d1_directionalblur_prop.htm
tech.root: Direct2D
ms.assetid: BEC82079-543E-4675-84DD-0DE7D852866E
ms.date: 12/05/2018
ms.keywords: D2D1_DIRECTIONALBLUR_PROP, D2D1_DIRECTIONALBLUR_PROP enumeration [Direct2D], D2D1_DIRECTIONALBLUR_PROP_ANGLE, D2D1_DIRECTIONALBLUR_PROP_BORDER_MODE, D2D1_DIRECTIONALBLUR_PROP_OPTIMIZATION, D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, d2d1effects/D2D1_DIRECTIONALBLUR_PROP, d2d1effects/D2D1_DIRECTIONALBLUR_PROP_ANGLE, d2d1effects/D2D1_DIRECTIONALBLUR_PROP_BORDER_MODE, d2d1effects/D2D1_DIRECTIONALBLUR_PROP_OPTIMIZATION, d2d1effects/D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, direct2d.d2d1_directionalblur_prop
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
req.typenames: D2D1_DIRECTIONALBLUR_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_DIRECTIONALBLUR_PROP
 - d2d1effects/D2D1_DIRECTIONALBLUR_PROP
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
 - D2D1_DIRECTIONALBLUR_PROP
---

# D2D1_DIRECTIONALBLUR_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/directional-blur">Directional blur effect</a>.

## -enum-fields

### -field D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION:0

The amount of blur to be applied to the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3. 
          The units of both the standard deviation and blur radius are DIPs. A value of 0 DIPs disables this effect. 
          

The type is FLOAT.

The default value is 3.0f.

### -field D2D1_DIRECTIONALBLUR_PROP_ANGLE:1

The angle of the blur relative to the x-axis, in the counterclockwise direction. The units are specified in degrees.
          

The blur kernel is first generated using the same process as for the Gaussian blur effect. The kernel values are then transformed according to the blur angle.

The type is FLOAT.

The default value is 0.0f.

### -field D2D1_DIRECTIONALBLUR_PROP_OPTIMIZATION:2

The optimization mode. See Optimization modes for more info.
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_directionalblur_optimization">D2D1_DIRECTIONALBLUR_OPTIMIZATION</a>.

The default value is D2D1_DIRECTIONALBLUR_OPTIMIZATION_BALANCED.

### -field D2D1_DIRECTIONALBLUR_PROP_BORDER_MODE:3

The mode used to calculate the border of the image, soft or hard. See Border modes for more info.
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_border_mode">D2D1_BORDER_MODE</a>.

The default value is D2D1_BORDER_MODE_SOFT.

### -field D2D1_DIRECTIONALBLUR_PROP_FORCE_DWORD:0xffffffff
