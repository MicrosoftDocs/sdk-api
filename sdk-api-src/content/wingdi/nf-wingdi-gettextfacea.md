---
UID: NF:wingdi.GetTextFaceA
title: GetTextFaceA function (wingdi.h)
description: The GetTextFace function retrieves the typeface name of the font that is selected into the specified device context. (ANSI)
helpviewer_keywords: ["GetTextFaceA", "wingdi/GetTextFaceA"]
old-location: gdi\gettextface.htm
tech.root: gdi
ms.assetid: c4c8c8f5-3651-481b-a55f-da7f49d92f3a
ms.date: 12/05/2018
ms.keywords: GetTextFace, GetTextFace function [Windows GDI], GetTextFaceA, GetTextFaceW, _win32_GetTextFace, gdi.gettextface, wingdi/GetTextFace, wingdi/GetTextFaceA, wingdi/GetTextFaceW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTextFaceW (Unicode) and GetTextFaceA (ANSI)
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
 - GetTextFaceA
 - wingdi/GetTextFaceA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-0.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetTextFace
 - GetTextFaceA
 - GetTextFaceW
---

# GetTextFaceA function


## -description

The <b>GetTextFace</b> function retrieves the typeface name of the font that is selected into the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param c [in]

The length of the buffer pointed to by <i>lpFaceName</i>. For the ANSI function it is a BYTE count and for the Unicode function it is a WORD count. Note that for the ANSI function, characters in SBCS code pages take one byte each, while most characters in DBCS code pages take two bytes; for the Unicode function, most currently defined Unicode characters (those in the Basic Multilingual Plane (BMP)) are one WORD while Unicode surrogates are two WORDs.

### -param lpName [out]

A pointer to the buffer that receives the typeface name. If this parameter is <b>NULL</b>, the function returns the number of characters in the name, including the terminating null character.

## -returns

If the function succeeds, the return value is the number of characters copied to the buffer.

If the function fails, the return value is zero.

## -remarks

The typeface name is copied as a null-terminated character string.

If the name is longer than the number of characters specified by the <i>nCount</i> parameter, the name is truncated.





> [!NOTE]
> The wingdi.h header defines GetTextFace as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextcolor">GetTextColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a">GetTextExtentPoint32</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextmetrics">GetTextMetrics</a>
