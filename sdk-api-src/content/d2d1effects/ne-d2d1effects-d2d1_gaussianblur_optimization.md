---
UID: NE:d2d1effects.D2D1_GAUSSIANBLUR_OPTIMIZATION
title: D2D1_GAUSSIANBLUR_OPTIMIZATION (d2d1effects.h)
description: The optimization mode for the Gaussian blur effect.
helpviewer_keywords: ["D2D1_GAUSSIANBLUR_OPTIMIZATION","D2D1_GAUSSIANBLUR_OPTIMIZATION enumeration [Direct2D]","D2D1_GAUSSIANBLUR_OPTIMIZATION_BALANCED","D2D1_GAUSSIANBLUR_OPTIMIZATION_QUALITY","D2D1_GAUSSIANBLUR_OPTIMIZATION_SPEED","d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION","d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION_BALANCED","d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION_QUALITY","d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION_SPEED","direct2d.d2d1_gaussianblur_optimization"]
old-location: direct2d\d2d1_gaussianblur_optimization.htm
tech.root: Direct2D
ms.assetid: D6A8BB3A-8286-4410-8EA3-A9AEA1797C5E
ms.date: 12/05/2018
ms.keywords: D2D1_GAUSSIANBLUR_OPTIMIZATION, D2D1_GAUSSIANBLUR_OPTIMIZATION enumeration [Direct2D], D2D1_GAUSSIANBLUR_OPTIMIZATION_BALANCED, D2D1_GAUSSIANBLUR_OPTIMIZATION_QUALITY, D2D1_GAUSSIANBLUR_OPTIMIZATION_SPEED, d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION, d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION_BALANCED, d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION_QUALITY, d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION_SPEED, direct2d.d2d1_gaussianblur_optimization
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
req.typenames: D2D1_GAUSSIANBLUR_OPTIMIZATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_GAUSSIANBLUR_OPTIMIZATION
 - d2d1effects/D2D1_GAUSSIANBLUR_OPTIMIZATION
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
 - D2D1_GAUSSIANBLUR_OPTIMIZATION
---

# D2D1_GAUSSIANBLUR_OPTIMIZATION enumeration


## -description

The optimization mode for the <a href="/windows/desktop/Direct2D/gaussian-blur">Gaussian blur effect</a>.

## -enum-fields

### -field D2D1_GAUSSIANBLUR_OPTIMIZATION_SPEED:0

Applies internal optimizations such as pre-scaling at relatively small radii. Uses linear filtering.

### -field D2D1_GAUSSIANBLUR_OPTIMIZATION_BALANCED:1

Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.

### -field D2D1_GAUSSIANBLUR_OPTIMIZATION_QUALITY:2

Only uses internal optimizations with large blur radii, where approximations are less likely to be visible. Uses trilinear filtering.

### -field D2D1_GAUSSIANBLUR_OPTIMIZATION_FORCE_DWORD:0xffffffff
