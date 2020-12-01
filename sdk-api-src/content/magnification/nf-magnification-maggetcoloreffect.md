---
UID: NF:magnification.MagGetColorEffect
title: MagGetColorEffect function (magnification.h)
description: Gets the color transformation matrix for a magnifier control.
old-location: magapi\magapi_MagGetColorEffect.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetcoloreffect.htm
ms.date: 12/05/2018
ms.keywords: MagGetColorEffect, MagGetColorEffect function [Magnification API], magapi.magapi_MagGetColorEffect, magapi_MagGetColorEffect, magnification/MagGetColorEffect
req.header: magnification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MagGetColorEffect
 - magnification/MagGetColorEffect
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
 - MagGetColorEffect
---

# MagGetColorEffect function


## -description

 Gets the color transformation matrix for a magnifier control.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The magnification window.

### -param pEffect [out]

Type: <b><a href="/windows/desktop/api/magnification/ns-magnification-magcoloreffect">PMAGCOLOREFFECT</a></b>

The color transformation matrix, or <b>NULL</b> if no color effect has been set.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

The magnifier control uses the color transformation matrix to apply a color effect to the entire magnifier window. 

This function requires Windows Display Driver Model (WDDM)-capable video cards.


#### Examples

The following example retrieves the color transformation matrix.


```cpp
// Description:
//   Retrieves the color transformation matrix from a magnifier control.
// Parameters:
//   hwndMag - handle of the magnifier control.
//
BOOL GetMagnifierColorTransform(HWND hwndMag)
{
    MAGCOLOREFFECT effect;

    BOOL ret = MagGetColorEffect(hwndMag, &effect);

    //
    // Do something with the color data.
    //

    return ret;
}

```

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetcoloreffect">MagSetColorEffect</a>