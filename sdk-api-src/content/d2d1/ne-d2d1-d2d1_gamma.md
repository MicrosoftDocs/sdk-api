---
UID: NE:d2d1.D2D1_GAMMA
title: D2D1_GAMMA (d2d1.h)
description: Specifies which gamma is used for interpolation.
helpviewer_keywords: ["D2D1_GAMMA","D2D1_GAMMA enumeration [Direct2D]","D2D1_GAMMA_1_0","D2D1_GAMMA_2_2","d2d1/D2D1_GAMMA","d2d1/D2D1_GAMMA_1_0","d2d1/D2D1_GAMMA_2_2","direct2d.D2D1_GAMMA"]
old-location: direct2d\D2D1_GAMMA.htm
tech.root: Direct2D
ms.assetid: c84c66c6-5f4a-41de-938c-76a409145971
ms.date: 12/05/2018
ms.keywords: D2D1_GAMMA, D2D1_GAMMA enumeration [Direct2D], D2D1_GAMMA_1_0, D2D1_GAMMA_2_2, d2d1/D2D1_GAMMA, d2d1/D2D1_GAMMA_1_0, d2d1/D2D1_GAMMA_2_2, direct2d.D2D1_GAMMA
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: D2D1_GAMMA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_GAMMA
 - d2d1/D2D1_GAMMA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_GAMMA
---

# D2D1_GAMMA enumeration


## -description

Specifies which gamma is used for interpolation.

## -enum-fields

### -field D2D1_GAMMA_2_2:0

Interpolation is performed in the standard RGB (sRGB) gamma.

### -field D2D1_GAMMA_1_0:1

Interpolation is performed in the linear-gamma color space.

### -field D2D1_GAMMA_FORCE_DWORD:0xffffffff

## -remarks

Interpolating in a linear gamma space (<b>D2D1_GAMMA_1_0</b>) can avoid changes in perceived brightness caused by the effect of gamma correction in spaces where the gamma is not 1.0, such as the default sRGB color space, where the gamma is 2.2. For an example of the differences between these two blending modes, consider the following illustration, which shows two gradients, each of which blends from red to blue to green:

<img alt="Illustration of two gradients from red to blue to green, blended by using sRGB gamma and linear-gamma" src="./images/D2D1_GAMMA.png"/>

The first gradient is interpolated linearly in the space of the render target (sRGB in this case), and one can see the dark bands between each color. The second gradient uses a gamma-correct linear interpolation, and thus does not exhibit the same variations in brightness.

