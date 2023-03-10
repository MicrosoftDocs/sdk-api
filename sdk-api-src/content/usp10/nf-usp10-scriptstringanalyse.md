---
UID: NF:usp10.ScriptStringAnalyse
title: ScriptStringAnalyse function (usp10.h)
description: Analyzes a plain text string.
helpviewer_keywords: ["SSA_BREAK","SSA_CLIP","SSA_DZWG","SSA_FALLBACK","SSA_FIT","SSA_GCP","SSA_GLYPHS","SSA_HIDEHOTKEY","SSA_HOTKEY","SSA_HOTKEYONLY","SSA_LINK","SSA_METAFILE","SSA_PASSWORD","SSA_RTL","SSA_TAB","ScriptStringAnalyse","ScriptStringAnalyse function [Internationalization for Windows Applications]","_win32_ScriptStringAnalyse","intl.scriptstringanalyse","usp10/ScriptStringAnalyse"]
old-location: intl\scriptstringanalyse.htm
tech.root: Intl
ms.assetid: 6d0e7070-159e-436b-85b5-cabb3da83f5e
ms.date: 12/05/2018
ms.keywords: SSA_BREAK, SSA_CLIP, SSA_DZWG, SSA_FALLBACK, SSA_FIT, SSA_GCP, SSA_GLYPHS, SSA_HIDEHOTKEY, SSA_HOTKEY, SSA_HOTKEYONLY, SSA_LINK, SSA_METAFILE, SSA_PASSWORD, SSA_RTL, SSA_TAB, ScriptStringAnalyse, ScriptStringAnalyse function [Internationalization for Windows Applications], _win32_ScriptStringAnalyse, intl.scriptstringanalyse, usp10/ScriptStringAnalyse
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
 - ScriptStringAnalyse
 - usp10/ScriptStringAnalyse
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
 - ScriptStringAnalyse
---

# ScriptStringAnalyse function


## -description

Analyzes a plain text string.

## -parameters

### -param hdc [in]

Handle to the device context. If <i>dwFlags</i> is set to SSA_GLYPHS, the device context handle is required. If <i>dwFlags</i> is set to SSA_BREAK, the device context handle is optional. If the device context handle is provided, the function inspects the current font in the device context. If the current font is a symbolic font, the function treats the character string as a single neutral SCRIPT_UNDEFINED item.

### -param pString [in]

Pointer to the string to analyze. The string must have at least one character. It can be a Unicode string or use the character set from a Windows ANSI <a href="/windows/desktop/Intl/code-pages">code page</a>, as specified by the <i>iCharset</i> parameter.

### -param cString [in]

Length of the string to analyze. The length is measured in characters for an ANSI string or in wide characters for a Unicode string. The length must be at least 1.

### -param cGlyphs [in]

Size of the glyph buffer, in WORD values. This size is required. The recommended size is <code>(1.5 * cString + 16)</code>.

### -param iCharset [in]

Character set descriptor. If the input string is an ANSI string, this descriptor is set to the character set identifier. If the string is a Unicode string, this descriptor is set to -1.

The following character set identifiers are defined:

### -param dwFlags [in]

Flags indicating the analysis that is required. This parameter can have one of the values listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SSA_BREAK"></a><a id="ssa_break"></a><dl>
<dt><b>SSA_BREAK</b></dt>
</dl>
</td>
<td width="60%">
Retrieve break flags, that is, character and word stops.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_CLIP"></a><a id="ssa_clip"></a><dl>
<dt><b>SSA_CLIP</b></dt>
</dl>
</td>
<td width="60%">
Clip the string at <i>iReqWidth.</i>

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_DZWG"></a><a id="ssa_dzwg"></a><dl>
<dt><b>SSA_DZWG</b></dt>
</dl>
</td>
<td width="60%">
Provide representation glyphs for control characters.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_FALLBACK"></a><a id="ssa_fallback"></a><dl>
<dt><b>SSA_FALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Use fallback fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_FIT"></a><a id="ssa_fit"></a><dl>
<dt><b>SSA_FIT</b></dt>
</dl>
</td>
<td width="60%">
Justify the string to <i>iReqWidth</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_GCP"></a><a id="ssa_gcp"></a><dl>
<dt><b>SSA_GCP</b></dt>
</dl>
</td>
<td width="60%">
Retrieve missing glyphs and <i>pwLogClust</i> with <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> conventions.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_GLYPHS"></a><a id="ssa_glyphs"></a><dl>
<dt><b>SSA_GLYPHS</b></dt>
</dl>
</td>
<td width="60%">
Generate glyphs, positions, and attributes.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_HIDEHOTKEY"></a><a id="ssa_hidehotkey"></a><dl>
<dt><b>SSA_HIDEHOTKEY</b></dt>
</dl>
</td>
<td width="60%">
Remove the first "&amp;" from displayed string.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_HOTKEY"></a><a id="ssa_hotkey"></a><dl>
<dt><b>SSA_HOTKEY</b></dt>
</dl>
</td>
<td width="60%">
Replace "&amp;" with underline on subsequent code point.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_HOTKEYONLY"></a><a id="ssa_hotkeyonly"></a><dl>
<dt><b>SSA_HOTKEYONLY</b></dt>
</dl>
</td>
<td width="60%">
Display underline only. The resulting bit pattern might be displayed, using an XOR mask, to toggle the visibility of the hotkey underline without disturbing the text.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_LINK"></a><a id="ssa_link"></a><dl>
<dt><b>SSA_LINK</b></dt>
</dl>
</td>
<td width="60%">
Apply East Asian font linking and association to noncomplex text.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_METAFILE"></a><a id="ssa_metafile"></a><dl>
<dt><b>SSA_METAFILE</b></dt>
</dl>
</td>
<td width="60%">
Write items with <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOutW</a> calls, not with glyphs.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_PASSWORD"></a><a id="ssa_password"></a><dl>
<dt><b>SSA_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
Duplicate input string containing a single character <i>cString</i> times.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_RTL"></a><a id="ssa_rtl"></a><dl>
<dt><b>SSA_RTL</b></dt>
</dl>
</td>
<td width="60%">
Use base embedding level 1.

</td>
</tr>
<tr>
<td width="40%"><a id="SSA_TAB"></a><a id="ssa_tab"></a><dl>
<dt><b>SSA_TAB</b></dt>
</dl>
</td>
<td width="60%">
Expand tabs.

</td>
</tr>
</table>

### -param iReqWidth [in]

Width required for fitting or clipping.

### -param psControl [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a> structure. The application can set this parameter to <b>NULL</b> to indicate that all <b>SCRIPT_CONTROL</b> members are set to 0.

### -param psState [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a> structure. The application can set this parameter to <b>NULL</b> to indicate that all <b>SCRIPT_STATE</b> members are set to 0. The <b>uBidiLevel</b> member of <b>SCRIPT_STATE</b> is ignored. The value used is derived from the SSA_RTL flag in combination with the layout of the device context.

### -param piDx [in, optional]

Pointer to the requested logical dx array.

### -param pTabdef [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_tabdef">SCRIPT_TABDEF</a> structure. This value is only required if <i>dwFlags</i> is set to SSA_TAB.

### -param pbInClass [in]

Pointer to a BYTE value that indicates <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> character classifications.

### -param pssa [out]

Pointer to a buffer in which this function retrieves a <a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a> structure. This structure is dynamically allocated on successful return from the function.

## -returns

Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed.

Error returns include:
    <ul>
<li>E_INVALIDARG. An invalid parameter is found.</li>
<li>USP_E_SCRIPT_NOT_IN_FONT. SSA_FALLBACK has not been specified, or a standard fallback font is missing.</li>
</ul>


The function can also return a system error converted to an HRESULT type. An example is an error returned due to lack of memory or a GDI call using the device context.

## -remarks

Use of this function is the first step in handling plain text strings. Such a string has only one font, one style, one size, one color, and so forth. <b>ScriptStringAnalyse</b> allocates temporary buffers for item analyses, glyphs, advance widths, and the like. Then it automatically runs <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>, <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>, <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>, and <a href="/windows/desktop/api/usp10/nf-usp10-scriptbreak">ScriptBreak</a>. The results are available through all the other <b>ScriptString*</b> functions.

On successful return from this function, <i>pssa</i> indicates a dynamically allocated structure that the application can pass successively to the other <b>ScriptString*</b> functions. The application must ultimately free the structure by calling <a href="/windows/desktop/api/usp10/nf-usp10-scriptstringfree">ScriptStringFree</a>.

Although the functionality of <b>ScriptStringAnalyse</b> can be implemented by direct calls to other functions, use of the function itself drastically reduces the amount of code required in the application for plain text handling.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a>



<a href="/windows/desktop/Intl/script-string-analysis">SCRIPT_STRING_ANALYSIS</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_tabdef">SCRIPT_TABDEF</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptbreak">ScriptBreak</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>