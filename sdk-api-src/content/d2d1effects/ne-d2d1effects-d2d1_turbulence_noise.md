---
UID: NE:d2d1effects.D2D1_TURBULENCE_NOISE
title: D2D1_TURBULENCE_NOISE (d2d1effects.h)
description: The turbulence noise mode for the Turbulence effect. Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.
helpviewer_keywords: ["D2D1_TURBULENCE_NOISE","D2D1_TURBULENCE_NOISE enumeration [Direct2D]","D2D1_TURBULENCE_NOISE_FRACTAL_SUM","D2D1_TURBULENCE_NOISE_TURBULENCE","d2d1effects/D2D1_TURBULENCE_NOISE","d2d1effects/D2D1_TURBULENCE_NOISE_FRACTAL_SUM","d2d1effects/D2D1_TURBULENCE_NOISE_TURBULENCE","direct2d.d2d1_turbulence_noise"]
old-location: direct2d\d2d1_turbulence_noise.htm
tech.root: Direct2D
ms.assetid: 6D2C57B9-AE6E-43CF-AF76-299BC7FCFC06
ms.date: 12/05/2018
ms.keywords: D2D1_TURBULENCE_NOISE, D2D1_TURBULENCE_NOISE enumeration [Direct2D], D2D1_TURBULENCE_NOISE_FRACTAL_SUM, D2D1_TURBULENCE_NOISE_TURBULENCE, d2d1effects/D2D1_TURBULENCE_NOISE, d2d1effects/D2D1_TURBULENCE_NOISE_FRACTAL_SUM, d2d1effects/D2D1_TURBULENCE_NOISE_TURBULENCE, direct2d.d2d1_turbulence_noise
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
req.typenames: D2D1_TURBULENCE_NOISE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_TURBULENCE_NOISE
 - d2d1effects/D2D1_TURBULENCE_NOISE
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
 - D2D1_TURBULENCE_NOISE
---

# D2D1_TURBULENCE_NOISE enumeration


## -description

The turbulence noise mode for the <a href="/windows/desktop/Direct2D/turbulence">Turbulence effect</a>. 
        Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.

## -enum-fields

### -field D2D1_TURBULENCE_NOISE_FRACTAL_SUM:0

Computes a sum of the octaves, shifting the output range from [-1, 1], to [0, 1].

### -field D2D1_TURBULENCE_NOISE_TURBULENCE:1

Computes a sum of the absolute value of each octave.

### -field D2D1_TURBULENCE_NOISE_FORCE_DWORD:0xffffffff
