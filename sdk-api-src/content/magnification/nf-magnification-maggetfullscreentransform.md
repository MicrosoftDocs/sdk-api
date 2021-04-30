---
UID: NF:magnification.MagGetFullscreenTransform
title: MagGetFullscreenTransform function (magnification.h)
description: Retrieves the magnification settings for the full-screen magnifier.
helpviewer_keywords: ["MagGetFullscreenTransform","MagGetFullscreenTransform function [Magnification API]","magapi.magapi_maggetfullscreentransform","magnification/MagGetFullscreenTransform"]
old-location: magapi\magapi_maggetfullscreentransform.htm
tech.root: magapi
ms.assetid: 6270047A-8823-41D6-AD57-72A7E60F3696
ms.date: 12/05/2018
ms.keywords: MagGetFullscreenTransform, MagGetFullscreenTransform function [Magnification API], magapi.magapi_maggetfullscreentransform, magnification/MagGetFullscreenTransform
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
 - MagGetFullscreenTransform
 - magnification/MagGetFullscreenTransform
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
 - MagGetFullscreenTransform
---

# MagGetFullscreenTransform function


## -description

Retrieves the magnification settings for the full-screen magnifier.

## -parameters

### -param pMagLevel [out]

Type: <b>float*</b>

The current magnification factor for the full-screen magnifier.  A value of 1.0 indicates that the screen content is not being magnified. A value above 1.0 indicates the scale factor for magnification. A value less than 1.0 is not valid.

### -param pxOffset [out]

Type: <b>int*</b>

The x-coordinate offset for the upper-left corner of the unmagnified view.  The offset is relative to the upper-left corner of the primary monitor, in unmagnified coordinates.

### -param pyOffset [out]

Type: <b>int*</b>

The y-coordinate offset for the upper-left corner of the unmagnified view.  The offset is relative to the upper-left corner of the primary monitor, in unmagnified coordinates.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.

## -remarks

The offsets are not affected by the current dots per inch (dpi) setting.


#### Examples

The following code snippet retrieves the magnification value and offsets for the full-screen magnifier.


```cpp
    // Get the current magnification level and offset.
    float  magLevel;
    int    xOffset, yOffset;

    if (!MagGetFullscreenTransform(&magLevel, &xOffset, &yOffset))
    {
        return E_FAIL;
    }
    
    // 
    // Do something with the magnification settings.
    //    

```

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetfullscreentransform">MagSetFullscreenTransform</a>