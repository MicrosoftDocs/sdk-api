---
UID: NF:usp10.ScriptItemizeOpenType
title: ScriptItemizeOpenType function (usp10.h)
description: Breaks a Unicode string into individually shapeable items and provides an array of feature tags for each shapeable item for OpenType processing.
helpviewer_keywords: ["ScriptItemizeOpenType","ScriptItemizeOpenType function [Internationalization for Windows Applications]","_win32_ScriptItemizeOpenType","intl.scriptitemizeopentype","usp10/ScriptItemizeOpenType"]
old-location: intl\scriptitemizeopentype.htm
tech.root: Intl
ms.assetid: da15d6b3-6725-43b8-9a2c-c19269a79d1e
ms.date: 12/05/2018
ms.keywords: ScriptItemizeOpenType, ScriptItemizeOpenType function [Internationalization for Windows Applications], _win32_ScriptItemizeOpenType, intl.scriptitemizeopentype, usp10/ScriptItemizeOpenType
req.header: usp10.h
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
req.lib: Usp10.lib
req.dll: Usp10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Usp10.dll version 1.600 or greater on Windows XP
ms.custom: 19H1
f1_keywords:
 - ScriptItemizeOpenType
 - usp10/ScriptItemizeOpenType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-usp10-l1-1-0.dll
 - usp10.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - ScriptItemizeOpenType
---

# ScriptItemizeOpenType function


## -description

Breaks a Unicode string into individually shapeable <a href="/windows/desktop/Intl/uniscribe-glossary">items</a> and provides an array of feature tags for each shapeable item for OpenType processing.

## -parameters

### -param pwcInChars [in]

Pointer to a Unicode string to itemize.

### -param cInChars [in]

Number of characters in <i>pwcInChars</i> to itemize.

### -param cMaxItems [in]

Maximum number of <a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a> structures defining items to process.

### -param psControl [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a> structure indicating the type of itemization to perform.

Alternatively, the application can set this parameter to <b>NULL</b> if no <a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a> properties are needed. For more information, see the Remarks section.

### -param psState [in, optional]

Pointer to a <a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a> structure indicating the initial bidirectional algorithm state.

Alternatively, the application can set this parameter to <b>NULL</b> if the script state is not needed. For more information, see the Remarks section.

### -param pItems [out]

Pointer to a buffer in which the function retrieves <a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a> structures representing the items that have been processed. The buffer should be  <code>(cMaxItems + 1) * sizeof(SCRIPT_ITEM)</code> bytes in length. It is invalid to call this function with a buffer that handles less than two <b>SCRIPT_ITEM</b> structures. The function always adds a terminal item to the item analysis array so that the length of the item with zero-based index "i" is always available as:

<code>pItems[i+1].iCharPos - pItems[i].iCharPos;</code>

### -param pScriptTags [out]

Pointer to a buffer in which the function retrieves an array of <a href="/windows/desktop/Intl/opentype-tag">OPENTYPE_TAG</a> structures representing script tags. The buffer should be  <code>cMaxItems * sizeof(OPENTYPE_TAG)</code> bytes in length.

<div class="alert"><b>Note</b>  When all characters in an item are neutral, the value of this parameter is SCRIPT_TAG_UNKNOWN (0x00000000). This can happen, for example, if an item consists entirely of punctuation.</div>
<div> </div>

### -param pcItems [out]

Pointer to the number of <a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a> structures processed.

## -returns

Returns 0 if successful. The function returns a nonzero HRESULT value if it does not succeed. In all error cases, no items are fully processed and no part of the output contains defined values. The application can test the return value with the <b>SUCCEEDED</b> and <b>FAILED</b> macros.

The function returns E_OUTOFMEMORY if the size indicated by <i>cMaxItems</i> is too small. The application can try calling the function again with a larger buffer.

The function returns E_INVALIDARG if one or more of the following conditions occur:

<ul>
<li><i>pwcInChars</i> is set to <b>NULL</b></li>
<li><i>cInChars</i> is 0</li>
<li><i>pItems</i> is set to <b>NULL</b></li>
<li><i>pScriptTags</i> is set to <b>NULL</b></li>
<li><i>cMaxItems</i> &lt; 2</li>
</ul>

## -remarks

<b>ScriptItemizeOpenType</b> is preferred over the older <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a> function. One advantage of <b>ScriptItemizeOpenType</b> is the availability of feature tags for each shapeable item.

See <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

The function delimits items by either a change of shaping engine or a change of direction.

The application can create multiple ranges, or runs that fall entirely within a single item, from each <a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a> structure retrieved by <b>ScriptItemizeOpenType</b>. However, it should not combine multiple items into a single run. When measuring or rendering, the application can call <a href="/windows/desktop/api/usp10/nf-usp10-scriptshapeopentype">ScriptShapeOpenType</a> for each run and must pass the corresponding <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> structure in the <a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a> structure retrieved by <b>ScriptItemizeOpenType</b>.

If the text handled by an application can include any right-to-left content, the application uses the <i>psControl</i> and <i>psState</i> parameters in calling <b>ScriptItemizeOpenType</b>. However, the application does not have to do this and can handle bidirectional text itself instead of relying on Uniscribe to do so. The <i>psControl</i> and <i>psState</i> parameters are useful in some strictly left-to-right scenarios, for example, when the <b>fLinkStringBefore</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a> is not specific to right-to-left scripts. The application sets <i>psControl</i> and <i>psState</i> to <b>NULL</b> to have <b>ScriptItemizeOpenType</b> break the Unicode string purely by character code.

The application can set all parameters to non-<b>NULL</b> values to have the function perform a full Unicode bidirectional analysis. To permit a correct Unicode bidirectional analysis, the <a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a> structure should be initialized according to the reading order at paragraph start, and <b>ScriptItemizeOpenType</b> should be passed the whole paragraph. In particular, the <b>uBidiLevel</b> member should be initialized to 0 for left-to-right and 1 for right-to-left.

The <b>fRTL</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a> is referenced in <a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a>. The <b>fNumeric</b> member of <a href="/windows/desktop/api/usp10/ns-usp10-script_properties">SCRIPT_PROPERTIES</a> is retrieved by <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetproperties">ScriptGetProperties</a>. These members together provide the same classification as the <b>lpClass</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-gcp_resultsa">GCP_RESULTS</a>, referenced by <i>lpResults</i> in <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>.

European digits U+0030 through U+0039 can be rendered as national digits, as shown in the following table.

<table>
<tr>
<th>SCRIPT_STATE.fDigitSubstitute</th>
<th>SCRIPT_CONTROL.fContextDigits</th>
<th>Digit shapes displayed for Unicode U+0030 through U+0039</th>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Any</td>
<td>European digits</td>
</tr>
<tr>
<td><b>TRUE</b></td>
<td><b>FALSE</b></td>
<td>As specified in <b>uDefaultLanguage</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a>.</td>
</tr>
<tr>
<td><b>TRUE</b></td>
<td><b>TRUE</b></td>
<td>As prior strong text, defaulting to <b>uDefaultLanguage</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a>.</td>
</tr>
</table>
 

In context digit mode, one of the following actions occurs:

<ul>
<li>If the script specified by <b>uDefaultLanguage</b> is in the same direction as the output, all digits encountered before the first letters are rendered in the language indicated by <b>uDefaultLanguage</b>.</li>
<li>If the script specified by <b>uDefaultLanguage</b> is in the opposite direction from the output, all digits encountered before the first letters are rendered in European digits.</li>
</ul>
For example, if <b>uDefaultLanguage</b> indicates LANG_ARABIC, initial digits are in Arabic-Indic in a right-to-left embedding. However they are in European digits in a left-to-right embedding.

For more information, see <a href="/windows/desktop/Intl/digit-shapes">Digit Shapes</a>.

The Unicode control characters and definitions, and their effects on <a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a> members, are provided in the following table. For more information on Unicode control characters, see the <a href="https://www.unicode.org/standard/standard.html">The Unicode Standard</a>.

<table>
<tr>
<th>Unicode control characters</th>
<th>Meaning</th>
<th>Effect on SCRIPT_STATE</th>
</tr>
<tr>
<td>NADS</td>
<td>Override European digits (NODS) with national digit shapes.</td>
<td>Set <b>fDigitSubstitute</b>.</td>
</tr>
<tr>
<td>NODS</td>
<td>Use nominal digit shapes, otherwise known as European digits. See NADS.</td>
<td>Clear <b>fDigitSubstitute</b>.</td>
</tr>
<tr>
<td>ASS</td>
<td>Activate swapping of symmetric pairs, for example, parentheses. For these characters, left and right are interpreted as opening and closing. This is the default. See ISS.</td>
<td>Clear <b>fInhibitSymSwap</b>.</td>
</tr>
<tr>
<td>ISS</td>
<td>Inhibit swapping of symmetric pairs. See ASS.</td>
<td>Set <b>fInhibitSymSwap</b>.</td>
</tr>
<tr>
<td>AAFS</td>
<td>Activate Arabic form shaping for Arabic presentation forms. See IAFS.</td>
<td>Set <b>fCharShape</b>.</td>
</tr>
<tr>
<td>IAFS</td>
<td>Inhibit Arabic form shaping, that is, ligatures and cursive connections, for Arabic presentation forms. Nominal Arabic characters are not affected. This is the default. See AAFS.</td>
<td>Clear <b>fCharShape</b>.</td>
</tr>
</table>
 

The <b>fArabicNumContext</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a> supports the context-sensitive display of numerals in Arabic script text. It indicates if digits are rendered using native Arabic script digit shapes or European digits. At the beginning of a paragraph, this member should normally be initialized to <b>TRUE</b> for an Arabic locale, or <b>FALSE</b> for any other locale. The function updates the script state it as it processes strong text.

The output parameter <i>pScriptTags</i> indicates an array with entries parallel to items. For each item, this function retrieves a script tag that should be used for shaping in all subsequent operations.

A script tag is usually determined by <b>ScriptItemizeOpenType</b> from input characters. If the function retrieves a specific script tag, the application should pass it to other functions without change. However, when characters are neutral (for example, digits) and the script cannot be determined, the application should choose an appropriate script tag, for example, based on font and language associated with text.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Intl/digit-shapes">Digit Shapes</a>



<a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_analysis">SCRIPT_ANALYSIS</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshapeopentype">ScriptShapeOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptsubstitutesingleglyph">ScriptSubstituteSingleGlyph</a>



<a href="/windows/desktop/Intl/uniscribe-functions">Uniscribe Functions</a>