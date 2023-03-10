---
UID: NF:usp10.ScriptTextOut
title: ScriptTextOut function (usp10.h)
description: Displays text for the specified script shape and place information.
helpviewer_keywords: ["ScriptTextOut","ScriptTextOut function [Internationalization for Windows Applications]","_win32_ScriptTextOut","intl.scripttextout","usp10/ScriptTextOut"]
old-location: intl\scripttextout.htm
tech.root: Intl
ms.assetid: 8d69caeb-4c02-4a9f-9dd5-ac3c13561a57
ms.date: 12/05/2018
ms.keywords: ScriptTextOut, ScriptTextOut function [Internationalization for Windows Applications], _win32_ScriptTextOut, intl.scripttextout, usp10/ScriptTextOut
req.header: usp10.h
req.include-header: 
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
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 5 or later on Windows Me/98/95
ms.custom: 19H1
f1_keywords:
 - ScriptTextOut
 - usp10/ScriptTextOut
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Usp10.dll
 - Ext-MS-Win-usp10-l1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptTextOut
---

# ScriptTextOut function


## -description

Displays text for the specified script shape and place information.

## -parameters

### -param hdc [in]

Handle to the device context. For more information, see <a href="/windows/desktop/Intl/caching">Caching</a>. Note that, unlike some other related Uniscribe functions, this function defines the handle as mandatory.

### -param psc [in, out]

Pointer to a <a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a> structure identifying the script cache.

### -param x [in]

Value of the x coordinate of the first glyph.

### -param y [in]

Value of the y coordinate of the first glyph.

### -param fuOptions [in]

Options equivalent to the <i>fuOptions</i> parameter of <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>. This parameter can be set to either ETO_CLIPPED or ETO_OPAQUE, to both values, or to neither value.

### -param lprc [in, optional]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the rectangle used to clip the display. The application can set this parameter to <b>NULL</b>.

### -param psa [in]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>.

### -param pwcReserved [in]

Reserved; must be set to <b>NULL</b>.

### -param iReserved [in]

Reserved; must be 0.

### -param pwGlyphs [in]

Pointer to an array of glyphs obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>.

### -param cGlyphs [in]

Count of the glyphs in the array indicated by <i>pwGlyphs</i>. The maximum number of glyphs is 65,536.

### -param piAdvance [in]

Pointer to an array of advance widths obtained from a previous call to <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>.

### -param piJustify [in, optional]

Pointer to an array of justified advance widths (cell widths). The application can set this parameter to <b>NULL</b>.

### -param pGoffset [in]

Pointer to a <a href="/windows/desktop/api/usp10/ns-usp10-goffset">GOFFSET</a> structure containing the x and y offsets for the combining glyph.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

## -remarks

This function calls the operating system <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> function for text display. For more information, see <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>.

All arrays are in display order unless the <b>fLogicalOrder</b> member is set in the <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure indicated by <i>psa</i>.

For any run that is rendered right-to-left and was generated in logical order by forcing the <b>fLogicalOrder</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>, the application must call <a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a> (hdc, TA_RIGHT) and give the right-side coordinate before calling <b>ScriptTextOut</b>.

The array indicated by <i>piJustify</i> provides cell widths for each glyph. When the width of a glyph differs from the unjustified width, specified by <i>piAdvance</i>, space is added to or removed from the glyph cell at its trailing edge. The glyph is always aligned with the leading edge of its cell. This rule applies even in visual order.

When a glyph cell is extended, the extra space is usually made up by the addition of white space. However, for Arabic scripts, the extra space is made up by one or more kashida glyphs, unless the extra space is insufficient for the shortest kashida glyph in the font. The width of the shortest kashida is available by calling <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontproperties">ScriptGetFontProperties</a>.

The application should pass a value for <i>piJustify</i> only if the string must be justified by <b>ScriptTextOut</b>. Normally, the application should pass <b>NULL</b>.

The application should not use <b>ScriptTextOut</b> to write to a metafile unless the metafile will be played back without any font substitution, for example, immediately on the same system for scalable page preview. <b>ScriptTextOut</b> records glyph numbers in the metafile. Since glyph numbers vary considerably from one font to another, the file is unlikely to play back correctly when different fonts are substituted. For example, when a metafile is played back at a different scale, a <a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a> request recorded in the metafile can resolve to a bitmap instead of a TrueType font. Likewise, if the metafile is played back on a different computer, the requested fonts might not be installed. To write complex scripts in a metafile in a font-independent manner, the application should use <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a> to write the logical characters directly, so that glyph generation and placement do not occur until the text is played back.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/desktop/api/usp10/ns-usp10-goffset">GOFFSET</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/desktop/Intl/script-cache">SCRIPT_CACHE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontproperties">ScriptGetFontProperties</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>