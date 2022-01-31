---
UID: NE:d2d1effects_2.D2D1_VIGNETTE_PROP
title: D2D1_VIGNETTE_PROP (d2d1effects_2.h)
description: Identifiers for properties of the Vignette effect.
helpviewer_keywords: ["D2D1_VIGNETTE_PROP","D2D1_VIGNETTE_PROP enumeration [Direct2D]","D2D1_VIGNETTE_PROP_COLOR","D2D1_VIGNETTE_PROP_STRENGTH","D2D1_VIGNETTE_PROP_TRANSITION_SIZE","d2d1effects_2/D2D1_VIGNETTE_PROP","d2d1effects_2/D2D1_VIGNETTE_PROP_COLOR","d2d1effects_2/D2D1_VIGNETTE_PROP_STRENGTH","d2d1effects_2/D2D1_VIGNETTE_PROP_TRANSITION_SIZE","direct2d.d2d1_vignette_prop"]
old-location: direct2d\d2d1_vignette_prop.htm
tech.root: Direct2D
ms.assetid: B45EFED7-97CA-41AF-9C36-4ECDCC153183
ms.date: 12/05/2018
ms.keywords: D2D1_VIGNETTE_PROP, D2D1_VIGNETTE_PROP enumeration [Direct2D], D2D1_VIGNETTE_PROP_COLOR, D2D1_VIGNETTE_PROP_STRENGTH, D2D1_VIGNETTE_PROP_TRANSITION_SIZE, d2d1effects_2/D2D1_VIGNETTE_PROP, d2d1effects_2/D2D1_VIGNETTE_PROP_COLOR, d2d1effects_2/D2D1_VIGNETTE_PROP_STRENGTH, d2d1effects_2/D2D1_VIGNETTE_PROP_TRANSITION_SIZE, direct2d.d2d1_vignette_prop
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
req.typenames: D2D1_VIGNETTE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_VIGNETTE_PROP
 - d2d1effects_2/D2D1_VIGNETTE_PROP
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
 - D2D1_VIGNETTE_PROP
---

# D2D1_VIGNETTE_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/vignette-effect">Vignette effect</a>.

## -enum-fields

### -field D2D1_VIGNETTE_PROP_COLOR:0

The D2D1_VIGNETTE_PROP_COLOR property is an RGB triplet that specifies the color to fade the image's edges to. The default color is black.

### -field D2D1_VIGNETTE_PROP_TRANSITION_SIZE:1

The D2D1_VIGNETTE_PROP_TRANSITION_SIZE property is a float value that specifies the size of the vignette region as a percentage of the full image region.  
          A size of 0 means the unfaded region is the entire image, while a size of 1 means the faded region is the entire source image.
          The allowed range is 0.0 to 1.0.  The default value is 0.1.

### -field D2D1_VIGNETTE_PROP_STRENGTH:2

The D2D1_VIGNETTE_PROP_STRENGTH property is a float value that specifies how much the vignette color bleeds in for a given transition size. 
          The allowed range is 0.0 to 1.0.  The default value is 0.5.

### -field D2D1_VIGNETTE_PROP_FORCE_DWORD:0xffffffff
