---
UID: NE:d2d1effects_2.D2D1_CHROMAKEY_PROP
title: D2D1_CHROMAKEY_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Chroma-key effect.
helpviewer_keywords: ["D2D1_CHROMAKEY_PROP","D2D1_CHROMAKEY_PROP enumeration [Direct2D]","D2D1_CHROMAKEY_PROP_COLOR","D2D1_CHROMAKEY_PROP_FEATHER","D2D1_CHROMAKEY_PROP_INVERT_ALPHA","D2D1_CHROMAKEY_PROP_TOLERANCE","d2d1effects_2/D2D1_CHROMAKEY_PROP","d2d1effects_2/D2D1_CHROMAKEY_PROP_COLOR","d2d1effects_2/D2D1_CHROMAKEY_PROP_FEATHER","d2d1effects_2/D2D1_CHROMAKEY_PROP_INVERT_ALPHA","d2d1effects_2/D2D1_CHROMAKEY_PROP_TOLERANCE","direct2d.d2d1_chromakey_prop"]
old-location: direct2d\d2d1_chromakey_prop.htm
tech.root: Direct2D
ms.assetid: B68F7F68-12F5-4650-84ED-D1EE0B670964
ms.date: 12/05/2018
ms.keywords: D2D1_CHROMAKEY_PROP, D2D1_CHROMAKEY_PROP enumeration [Direct2D], D2D1_CHROMAKEY_PROP_COLOR, D2D1_CHROMAKEY_PROP_FEATHER, D2D1_CHROMAKEY_PROP_INVERT_ALPHA, D2D1_CHROMAKEY_PROP_TOLERANCE, d2d1effects_2/D2D1_CHROMAKEY_PROP, d2d1effects_2/D2D1_CHROMAKEY_PROP_COLOR, d2d1effects_2/D2D1_CHROMAKEY_PROP_FEATHER, d2d1effects_2/D2D1_CHROMAKEY_PROP_INVERT_ALPHA, d2d1effects_2/D2D1_CHROMAKEY_PROP_TOLERANCE, direct2d.d2d1_chromakey_prop
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
req.typenames: D2D1_CHROMAKEY_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_CHROMAKEY_PROP
 - d2d1effects_2/D2D1_CHROMAKEY_PROP
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
 - D2D1_CHROMAKEY_PROP
---

# D2D1_CHROMAKEY_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/chromakey-effect">Chroma-key effect</a>.

## -enum-fields

### -field D2D1_CHROMAKEY_PROP_COLOR:0

The D2D1_CHROMAKEY_PROP_COLOR property is a vector4 value indicating the color that should be converted to alpha.  The default color is black.

### -field D2D1_CHROMAKEY_PROP_TOLERANCE:1

The D2D1_CHROMAKEY_PROP_TOLERANCE property is a float value indicating the tolerance for matching the color specified in the D2D1_CHROMAKEY_PROP_COLOR property.  
          The allowed range is 0.0 to 1.0.  The default value is 0.1.

### -field D2D1_CHROMAKEY_PROP_INVERT_ALPHA:2

The D2D1_CHROMAKEY_PROP_INVERT_ALPHA property is a boolean value indicating whether the alpha values should be inverted.  The default value if False.

### -field D2D1_CHROMAKEY_PROP_FEATHER:3

The D2D1_CHROMAKEY_PROP_FEATHER property is a boolean value whether the edges of the output should be softened in the alpha channel.
          When set to False, the alpha output by the effect is 1-bit: either fully opaque or fully transparent. Setting to True results in a softening of edges in the alpha channel of the Chroma Key output.
          The default value is False.

### -field D2D1_CHROMAKEY_PROP_FORCE_DWORD:0xffffffff
