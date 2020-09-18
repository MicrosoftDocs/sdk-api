---
UID: NF:magnification.MagGetFullscreenColorEffect
title: MagGetFullscreenColorEffect function (magnification.h)
description: Retrieves the color transformation matrix associated with the full-screen magnifier.
helpviewer_keywords: ["MagGetFullscreenColorEffect","MagGetFullscreenColorEffect function [Magnification API]","magapi.magapi_maggetfullscreencoloreffect","magnification/MagGetFullscreenColorEffect"]
old-location: magapi\magapi_maggetfullscreencoloreffect.htm
tech.root: magapi
ms.assetid: 1C37DB20-1267-447B-A34F-E3EC83F51907
ms.date: 12/05/2018
ms.keywords: MagGetFullscreenColorEffect, MagGetFullscreenColorEffect function [Magnification API], magapi.magapi_maggetfullscreencoloreffect, magnification/MagGetFullscreenColorEffect
req.header: magnification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MagGetFullscreenColorEffect
 - magnification/MagGetFullscreenColorEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagGetFullscreenColorEffect
---

# MagGetFullscreenColorEffect function


## -description

Retrieves the color transformation matrix  associated with the  full-screen magnifier.

## -parameters

### -param pEffect [out]

Type: <b><a href="/windows/desktop/api/magnification/ns-magnification-magcoloreffect">PMAGCOLOREFFECT</a></b>

The color transformation matrix, or the identity matrix if no color effect has been set.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.

## -remarks

The full-screen magnifier uses the color transformation matrix to apply a color effect to the entire screen.


#### Examples

The following example retrieves the color transformation matrix associated with the full-screen magnifier.


```cpp
        // Get the current color effect.
        MAGCOLOREFFECT magEffect;

        if (!MagGetFullscreenColorEffect(&magEffect))
            return E_FAIL;

```

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetfullscreencoloreffect">MagSetFullscreenColorEffect</a>