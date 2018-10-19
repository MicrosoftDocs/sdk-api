---
UID: NE:d2d1effects.D2D1_DIRECTIONALBLUR_OPTIMIZATION
title: D2D1_DIRECTIONALBLUR_OPTIMIZATION
author: windows-sdk-content
description: Specifies the optimization mode for the Directional blur effect.
old-location: direct2d\d2d1_directionalblur_optimization.htm
tech.root: direct2d
ms.assetid: 28B99069-3380-4D44-82A1-9A8F551B3C45
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: D2D1_DIRECTIONALBLUR_OPTIMIZATION, D2D1_DIRECTIONALBLUR_OPTIMIZATION enumeration [Direct2D], D2D1_DIRECTIONALBLUR_OPTIMIZATION_BALANCED, D2D1_DIRECTIONALBLUR_OPTIMIZATION_QUALITY, D2D1_DIRECTIONALBLUR_OPTIMIZATION_SPEED, d2d1effects/D2D1_DIRECTIONALBLUR_OPTIMIZATION, d2d1effects/D2D1_DIRECTIONALBLUR_OPTIMIZATION_BALANCED, d2d1effects/D2D1_DIRECTIONALBLUR_OPTIMIZATION_QUALITY, d2d1effects/D2D1_DIRECTIONALBLUR_OPTIMIZATION_SPEED, direct2d.d2d1_directionalblur_optimization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_DIRECTIONALBLUR_OPTIMIZATION
product: Windows
targetos: Windows
req.typenames: D2D1_DIRECTIONALBLUR_OPTIMIZATION
req.redist: 
---

# D2D1_DIRECTIONALBLUR_OPTIMIZATION enumeration


## -description


Specifies the optimization mode for the <a href="https://msdn.microsoft.com/en-us/library/Hh706328(v=VS.85).aspx">Directional blur effect</a>.


## -enum-fields




### -field D2D1_DIRECTIONALBLUR_OPTIMIZATION_SPEED

Applies internal optimizations such as pre-scaling at relatively small radii. Uses linear filtering.


### -field D2D1_DIRECTIONALBLUR_OPTIMIZATION_BALANCED

Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.


### -field D2D1_DIRECTIONALBLUR_OPTIMIZATION_QUALITY

Only uses internal optimizations with large blur radii, where approximations are less likely to be visible. Uses trilinear filtering.


### -field D2D1_DIRECTIONALBLUR_OPTIMIZATION_FORCE_DWORD



