---
UID: NF:wingdi.EnumFontsW
title: EnumFontsW function (wingdi.h)
description: The EnumFonts function enumerates the fonts available on a specified device. (Unicode)
helpviewer_keywords: ["EnumFonts", "EnumFonts function [Windows GDI]", "EnumFontsW", "_win32_EnumFonts", "gdi.enumfonts", "wingdi/EnumFonts", "wingdi/EnumFontsW"]
old-location: gdi\enumfonts.htm
tech.root: gdi
ms.assetid: b5dfc38d-c400-4900-a15b-f251815ee346
ms.date: 12/05/2018
ms.keywords: EnumFonts, EnumFonts function [Windows GDI], EnumFontsA, EnumFontsW, _win32_EnumFonts, gdi.enumfonts, wingdi/EnumFonts, wingdi/EnumFontsA, wingdi/EnumFontsW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumFontsW (Unicode) and EnumFontsA (ANSI)
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
 - EnumFontsW
 - wingdi/EnumFontsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-L1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - EnumFonts
 - EnumFontsA
 - EnumFontsW
---

# EnumFontsW function


## -description

The <b>EnumFonts</b> function enumerates the fonts available on a specified device. For each font with the specified typeface name, the <b>EnumFonts</b> function retrieves information about that font and passes it to the application defined callback function. This callback function can process the font information as desired. Enumeration continues until there are no more fonts or the callback function returns zero.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> function.</div><div> </div>

## -parameters

### -param hdc [in]

A handle to the device context from which to enumerate the fonts.

### -param lpLogfont [in]

A pointer to a null-terminated string that specifies the typeface name of the desired fonts. If <i>lpFaceName</i> is <b>NULL</b>, <b>EnumFonts</b> randomly selects and enumerates one font of each available typeface.

### -param lpProc [in]

A pointer to the application definedcallback function. For more information, see <a href="/previous-versions/dd162623(v=vs.85)">EnumFontsProc</a>.

### -param lParam [in]

A pointer to any application-defined data. The data is passed to the callback function along with the font information.

## -returns

The return value is the last value returned by the callback function. Its meaning is defined by the application.

## -remarks

Use <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> instead of <b>EnumFonts</b>. The <b>EnumFontFamiliesEx</b> function differs from the <b>EnumFonts</b> function in that it retrieves the style names associated with a TrueType font. With <b>EnumFontFamiliesEx</b>, you can retrieve information about font styles that cannot be enumerated using the <b>EnumFonts</b> function.

The fonts for many East Asian languages have two typeface names: an English name and a localized name. <b>EnumFonts</b>, <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> return the English typeface name if the system locale does not match the language of the font.





> [!NOTE]
> The wingdi.h header defines EnumFonts as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesa">EnumFontFamilies</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="/previous-versions/dd162623(v=vs.85)">EnumFontsProc</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>
