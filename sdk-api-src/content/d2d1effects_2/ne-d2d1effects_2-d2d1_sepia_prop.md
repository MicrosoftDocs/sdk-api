---
UID: NE:d2d1effects_2.D2D1_SEPIA_PROP
title: D2D1_SEPIA_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Sepia effect.
helpviewer_keywords: ["D2D1_SEPIA_PROP","D2D1_SEPIA_PROP enumeration [Direct2D]","D2D1_SEPIA_PROP_ALPHA_MODE","D2D1_SEPIA_PROP_INTENSITY","d2d1effects_2/D2D1_SEPIA_PROP","d2d1effects_2/D2D1_SEPIA_PROP_ALPHA_MODE","d2d1effects_2/D2D1_SEPIA_PROP_INTENSITY","direct2d.d2d1_sepia_prop"]
old-location: direct2d\d2d1_sepia_prop.htm
tech.root: Direct2D
ms.assetid: 159897D5-DB46-46B7-A88B-CC57D1AC8DE5
ms.date: 12/05/2018
ms.keywords: D2D1_SEPIA_PROP, D2D1_SEPIA_PROP enumeration [Direct2D], D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_SEPIA_PROP_INTENSITY, d2d1effects_2/D2D1_SEPIA_PROP, d2d1effects_2/D2D1_SEPIA_PROP_ALPHA_MODE, d2d1effects_2/D2D1_SEPIA_PROP_INTENSITY, direct2d.d2d1_sepia_prop
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
req.typenames: D2D1_SEPIA_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SEPIA_PROP
 - d2d1effects_2/D2D1_SEPIA_PROP
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
 - D2D1_SEPIA_PROP
---

# D2D1_SEPIA_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/sepia-effect">Sepia effect</a>.

## -enum-fields

### -field D2D1_SEPIA_PROP_INTENSITY:0

The D2D1_SEPIA_PROP_INTENSITY property is a float value indicating the intensity of the sepia effect. The allowed range is 0.0 to 1.0.  The default value is 0.5.

### -field D2D1_SEPIA_PROP_ALPHA_MODE:1

The D2D1_SEPIA_PROP_ALPHA_MODE property is a <a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE</a> enumeration value indicating the alpha mode of the input file.
          See the About Alpha Modes section of the <a href="/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a> topic for additional information..  
          The default value is D2D1_ALPHA_MODE_PREMULTIPLIED.

### -field D2D1_SEPIA_PROP_FORCE_DWORD:0xffffffff
