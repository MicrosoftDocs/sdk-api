---
UID: NF:wingdi.SetMapperFlags
title: SetMapperFlags function (wingdi.h)
description: The SetMapperFlags function alters the algorithm the font mapper uses when it maps logical fonts to physical fonts.
helpviewer_keywords: ["SetMapperFlags","SetMapperFlags function [Windows GDI]","_win32_SetMapperFlags","gdi.setmapperflags","wingdi/SetMapperFlags"]
old-location: gdi\setmapperflags.htm
tech.root: gdi
ms.assetid: 74cfe0d3-0d20-4382-8e76-55a6e2323308
ms.date: 12/05/2018
ms.keywords: SetMapperFlags, SetMapperFlags function [Windows GDI], _win32_SetMapperFlags, gdi.setmapperflags, wingdi/SetMapperFlags
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetMapperFlags
 - wingdi/SetMapperFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetMapperFlags
---

# SetMapperFlags function


## -description

The <b>SetMapperFlags</b> function alters the algorithm the font mapper uses when it maps logical fonts to physical fonts.

## -parameters

### -param hdc [in]

A handle to the device context that contains the font-mapper flag.

### -param flags [in]

Specifies whether the font mapper should attempt to match a font's aspect ratio to the current device's aspect ratio. If bit zero is set, the mapper selects only matching fonts.

## -returns

If the function succeeds, the return value is the previous value of the font-mapper flag.

If the function fails, the return value is GDI_ERROR.

## -remarks

If the <i>dwFlag</i> parameter is set and no matching fonts exist, Windows chooses a new aspect ratio and retrieves a font that matches this ratio.

The remaining bits of the <i>dwFlag</i> parameter must be zero.

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getaspectratiofilterex">GetAspectRatioFilterEx</a>