---
UID: NF:magnification.MagSetFullscreenColorEffect
title: MagSetFullscreenColorEffect function (magnification.h)
description: Changes the color transformation matrix associated with the full-screen magnifier.
helpviewer_keywords: ["MagSetFullscreenColorEffect","MagSetFullscreenColorEffect function [Magnification API]","magapi.magapi_magsetfullscreencoloreffect","magnification/MagSetFullscreenColorEffect"]
old-location: magapi\magapi_magsetfullscreencoloreffect.htm
tech.root: magapi
ms.assetid: F6CE5453-E427-46E4-81E8-6E96BA28C05C
ms.date: 12/05/2018
ms.keywords: MagSetFullscreenColorEffect, MagSetFullscreenColorEffect function [Magnification API], magapi.magapi_magsetfullscreencoloreffect, magnification/MagSetFullscreenColorEffect
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
 - MagSetFullscreenColorEffect
 - magnification/MagSetFullscreenColorEffect
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
 - MagSetFullscreenColorEffect
---

# MagSetFullscreenColorEffect function


## -description

Changes the color transformation matrix  associated with the full-screen magnifier.

## -parameters

### -param pEffect [in]

Type: <b><a href="/windows/desktop/api/magnification/ns-magnification-magcoloreffect">PMAGCOLOREFFECT</a></b>

The new color transformation matrix. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.

## -remarks

The full-screen magnifier uses the color transformation matrix to apply a color effect to the entire desktop. If the function is called multiple times, the most recent color transform is used. 


#### Examples

The following example defines two color transformation matrices for use with <b>MagSetFullscreenColorEffect</b>. The <code>g_MagEffectGrayscale</code> matrix converts the screen colors to grayscale. The <code>g_MagEffectIdentity</code> matrix is the identity matrix, which restores the original screen colors.


```cpp
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &g_MagEffectGrayscale : &g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}

```

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-maggetfullscreencoloreffect">MagGetFullscreenColorEffect</a>