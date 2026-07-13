---
UID: NF:wingdi.CreateColorSpaceW
title: CreateColorSpaceW function (wingdi.h)
description: The CreateColorSpace function creates a logical color space. (Unicode)
helpviewer_keywords: ["CreateColorSpace", "CreateColorSpace function [Windows Color System]", "CreateColorSpaceW", "_color_CreateColorSpace", "wcs.createcolorspace", "wingdi/CreateColorSpace", "wingdi/CreateColorSpaceW"]
old-location: wcs\createcolorspace.htm
tech.root: WCS
ms.assetid: c3fc798c-4bb9-4010-87d4-edc0005b7698
ms.date: 12/05/2018
ms.keywords: CreateColorSpace, CreateColorSpace function [Windows Color System], CreateColorSpaceA, CreateColorSpaceW, _color_CreateColorSpace, wcs.createcolorspace, wingdi/CreateColorSpace, wingdi/CreateColorSpaceA, wingdi/CreateColorSpaceW
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateColorSpaceW (Unicode) and CreateColorSpaceA (ANSI)
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
 - CreateColorSpaceW
 - wingdi/CreateColorSpaceW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateColorSpace
 - CreateColorSpaceA
 - CreateColorSpaceW
---

# CreateColorSpaceW function


## -description

The <b>CreateColorSpace</b> function creates a logical [color space](/windows/win32/wcs/c#color-space).

## -parameters

### -param lplcs

Pointer to the <a href="/windows/desktop/api/wingdi/ns-wingdi-logcolorspacea">LOGCOLORSPACE</a> data structure.

## -returns

If this function succeeds, the return value is a handle that identifies a color space.

If this function fails, the return value is <b>NULL</b>.

## -remarks

When the color space is no longer needed, use <b>DeleteColorSpace</b> to delete it.

<b>Windows 95/98/Me: </b><b>CreateColorSpaceW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.





> [!NOTE]
> The wingdi.h header defines CreateColorSpace as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [DeleteColorSpaceW](/windows/win32/api/wingdi/nf-wingdi-deletecolorspace)
