---
UID: NF:wingdi.EnumFontFamiliesW
title: EnumFontFamiliesW function (wingdi.h)
description: The EnumFontFamilies function enumerates the fonts in a specified font family that are available on a specified device. (Unicode)
helpviewer_keywords: ["EnumFontFamilies", "EnumFontFamilies function [Windows GDI]", "EnumFontFamiliesW", "_win32_EnumFontFamilies", "gdi.enumfontfamilies", "wingdi/EnumFontFamilies", "wingdi/EnumFontFamiliesW"]
old-location: gdi\enumfontfamilies.htm
tech.root: gdi
ms.assetid: 4960afbb-eeba-4030-ac89-d1ff077bb2f3
ms.date: 12/05/2018
ms.keywords: EnumFontFamilies, EnumFontFamilies function [Windows GDI], EnumFontFamiliesA, EnumFontFamiliesW, _win32_EnumFontFamilies, gdi.enumfontfamilies, wingdi/EnumFontFamilies, wingdi/EnumFontFamiliesA, wingdi/EnumFontFamiliesW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumFontFamiliesW (Unicode) and EnumFontFamiliesA (ANSI)
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
 - EnumFontFamiliesW
 - wingdi/EnumFontFamiliesW
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - EnumFontFamilies
 - EnumFontFamiliesA
 - EnumFontFamiliesW
---

# EnumFontFamiliesW function


## -description

The <b>EnumFontFamilies</b> function enumerates the fonts in a specified font family that are available on a specified device.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> function.</div><div> </div>

## -parameters

### -param hdc [in]

A handle to the device context from which to enumerate the fonts.

### -param lpLogfont [in]

A pointer to a null-terminated string that specifies the family name of the desired fonts. If <i>lpszFamily</i> is <b>NULL</b>, <b>EnumFontFamilies</b> selects and enumerates one font of each available type family.

### -param lpProc [in]

A pointer to the application defined callback function. For information, see <a href="/previous-versions/dd162621(v=vs.85)">EnumFontFamProc</a>.

### -param lParam [in]

A pointer to application-supplied data. The data is passed to the callback function along with the font information.

## -returns

The return value is the last value returned by the callback function. Its meaning is implementation specific.

## -remarks

For each font having the typeface name specified by the <i>lpszFamily</i> parameter, the <b>EnumFontFamilies</b> function retrieves information about that font and passes it to the function pointed to by the <i>lpEnumFontFamProc</i> parameter. The application defined callback function can process the font information as desired. Enumeration continues until there are no more fonts or the callback function returns zero.

When the graphics mode on the device context is set to GM_ADVANCED using the SetGraphicsMode function and the DEVICE_FONTTYPE flag is passed to the FontType parameter, this function returns a list of type 1 and OpenType fonts on the system. When the graphics mode is not set to GM_ADVANCED, this function returns a list of type 1, OpenType, and TrueType fonts on the system.

The fonts for many East Asian languages have two typeface names: an English name and a localized name. <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>, <b>EnumFontFamilies</b>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a> return the English typeface name if the system locale does not match the language of the font.


#### Examples

For examples, see <a href="/windows/desktop/gdi/enumerating-the-installed-fonts">Enumerating the Installed Fonts</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines EnumFontFamilies as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/dd162621(v=vs.85)">EnumFontFamProc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontfamiliesexa">EnumFontFamiliesEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumfontsa">EnumFonts</a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>
