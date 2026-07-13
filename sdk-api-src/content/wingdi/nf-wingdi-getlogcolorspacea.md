---
UID: NF:wingdi.GetLogColorSpaceA
title: GetLogColorSpaceA function (wingdi.h)
description: The GetLogColorSpace function retrieves the color space definition identified by a specified handle. (ANSI)
helpviewer_keywords: ["GetLogColorSpaceA", "wingdi/GetLogColorSpaceA"]
old-location: wcs\getlogcolorspace.htm
tech.root: WCS
ms.assetid: 01862a48-8c2f-4b29-b928-2800c02218a2
ms.date: 12/05/2018
ms.keywords: GetLogColorSpace, GetLogColorSpace function [Windows Color System], GetLogColorSpaceA, GetLogColorSpaceW, _color_GetLogColorSpace, wcs.getlogcolorspace, wingdi/GetLogColorSpace, wingdi/GetLogColorSpaceA, wingdi/GetLogColorSpaceW
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetLogColorSpaceW (Unicode) and GetLogColorSpaceA (ANSI)
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
 - GetLogColorSpaceA
 - wingdi/GetLogColorSpaceA
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
 - GetLogColorSpace
 - GetLogColorSpaceA
 - GetLogColorSpaceW
---

# GetLogColorSpaceA function


## -description

The <b>GetLogColorSpace</b> function retrieves the [color space](/windows/win32/wcs/c#color-space) definition identified by a specified handle.

## -parameters

### -param hColorSpace

Specifies the handle to a color space.

### -param lpBuffer

Points to a buffer to receive the <a href="/windows/desktop/api/wingdi/ns-wingdi-logcolorspacea">LOGCOLORSPACE</a> structure.

### -param nSize

Specifies the maximum size of the buffer.

## -returns

If this function succeeds, the return value is TRUE.

If this function fails, the return value is <b>FALSE</b>.

## -remarks

<b>Windows 95/98/Me: </b><b>GetLogColorSpaceW</b> is supported by the Microsoft Layer for Unicode. To use this, you must add certain files to your application, as outlined in <a href="https://msdn.microsoft.com/library?url=/library/mslu/winprog/microsoft_layer_for_unicode_on_windows_95_98_me_systems.asp">Microsoft Layer for Unicode on Windows 95/98/Me Systems</a>.





> [!NOTE]
> The wingdi.h header defines GetLogColorSpace as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
