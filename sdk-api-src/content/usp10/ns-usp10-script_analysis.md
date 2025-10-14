---
UID: NS:usp10.tag_SCRIPT_ANALYSIS
title: SCRIPT_ANALYSIS (usp10.h)
description: Contains a portion of a Unicode string, that is, an &quot;item&quot;.
helpviewer_keywords: ["FALSE","SCRIPT_ANALYSIS","SCRIPT_ANALYSIS structure [Internationalization for Windows Applications]","TRUE","_win32_SCRIPT_ANALYSIS_str","intl.script_analysis","usp10/SCRIPT_ANALYSIS"]
old-location: intl\script_analysis.htm
tech.root: Intl
ms.assetid: c673d5cc-c4ca-4238-8090-55abe3db324b
ms.date: 12/05/2018
ms.keywords: FALSE, SCRIPT_ANALYSIS, SCRIPT_ANALYSIS structure [Internationalization for Windows Applications], TRUE, _win32_SCRIPT_ANALYSIS_str, intl.script_analysis, usp10/SCRIPT_ANALYSIS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SCRIPT_ANALYSIS
req.redist: Internet Explorer 5 or later onWindows Me/98/95
ms.custom: 19H1
f1_keywords:
 - tag_SCRIPT_ANALYSIS
 - usp10/tag_SCRIPT_ANALYSIS
 - SCRIPT_ANALYSIS
 - usp10/SCRIPT_ANALYSIS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usp10.h
api_name:
 - SCRIPT_ANALYSIS
---

# SCRIPT_ANALYSIS structure


## -description

Contains a portion of a Unicode string, that is, an "item".

## -struct-fields

### -field eScript

Opaque value identifying the engine that Uniscribe uses when calling the <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>, <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>, and <a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a> functions for the item. The value for this member is undefined and applications should not rely on its value being the same from one release to the next. An application can obtain the attributes of <b>eScript</b> by calling <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetproperties">ScriptGetProperties</a>.

To disable shaping, the application should set this member to SCRIPT_UNDEFINED.

### -field fRTL

Value indicating rendering direction. Possible values are defined in the following table. This member is set to <b>TRUE</b> for a number in a left-to-right run, because digits are always displayed left to right, or <b>FALSE</b> for a number in a right-to-left run. The value of this member is normally identical to the parity of the Unicode embedding level, but it might differ if overridden by <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> legacy support.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Use a right-to-left rendering direction.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Use a left-to-right rendering direction.

</td>
</tr>
</table>

### -field fLayoutRTL

Value indicating layout direction for a number. Possible values are defined in the following table. This member is usually the same as the value assigned to <b>fRTL</b> for a number in a right-to-left run.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Lay out the number in a right-to-left run, because it is read as part of the right-to-left sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Lay out the number in a left-to-right run, because it is read as part of the left-to-right sequence.

</td>
</tr>
</table>

### -field fLinkBefore

Value indicating if the shaping engine shapes the first character of the item as if it joins with a previous character. Possible values are defined in the following table. This member is set by <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>. The application can override the value before calling <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Shape the first character by linking with a previous character.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not shape the first character by linking with a previous character.

</td>
</tr>
</table>

### -field fLinkAfter

Value indicating if the shaping engine shapes the last character of the item as if it joins with a subsequent character. Possible values are defined in the following table. This member is set by <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>. The application can override the value before calling <b>ScriptItemize</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Shape the last character by linking with a subsequent character.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not shape the last character by linking with a subsequent character.

</td>
</tr>
</table>

### -field fLogicalOrder

Value indicating if the shaping engine generates all glyph-related arrays in logical order. Possible values are defined in the following table. This member is set to <b>FALSE</b> by <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>. The application can override the value before calling <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Generate all glyph-related arrays in logical order.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Generate all glyph-related arrays in visual order, with the first array entry corresponding to the leftmost glyph. This value is the default.

</td>
</tr>
</table>

### -field fNoGlyphIndex

Value indicating the use of glyphs for the item. Possible values are defined in the following table. The application can set this member to <b>TRUE</b> on input to <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> to disable the use of glyphs for the item. Additionally, <b>ScriptShape</b> sets it to <b>TRUE</b> for a hardware context containing symbolic, unrecognized, and device fonts.

Disabling the use of glyphs also disables complex script shaping. Setting this member to <b>TRUE</b> implements shaping and placing directly by calls to <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextextentexpointa">GetTextExtentExPoint</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-exttextouta">ExtTextOut</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Disable the use of glyphs for the item. This value is used for bitmap, vector, and device fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Enable the use of glyphs for the item. This value is the default.

</td>
</tr>
</table>

### -field s

A <a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a> structure containing a copy of the Unicode algorithm state.

## -remarks

This structure is filled by <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a> or <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>, each of which breaks a Unicode string into individually shapeable items. Neither function accesses the <b>SCRIPT_ANALYSIS</b> structure directly. Each function handles an array of <a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a> structures, each of which has a member defining a <b>SCRIPT_ANALYSIS</b> structure.

Applications that use <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a> instead of <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a> should also use <a href="/windows/desktop/api/usp10/nf-usp10-scriptshapeopentype">ScriptShapeOpenType</a> and <a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a> instead of <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> and <a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>. For more information, see <a href="/windows/desktop/Intl/displaying-text-with-uniscribe">Displaying Text with Uniscribe</a>.

## -see-also

<a href="/windows/win32/api/usp10/ns-usp10-script_item">SCRIPT_ITEM</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptgetproperties">ScriptGetProperties</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype">ScriptItemizeOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplace">ScriptPlace</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptplaceopentype">ScriptPlaceOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshapeopentype">ScriptShapeOpenType</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scripttextout">ScriptTextOut</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>