---
UID: NS:usp10.tag_SCRIPT_STATE
title: SCRIPT_STATE (usp10.h)
description: Contains script state information.
helpviewer_keywords: ["FALSE","SCRIPT_STATE","SCRIPT_STATE structure [Internationalization for Windows Applications]","TRUE","_win32_SCRIPT_STATE_str","intl.script_state","usp10/SCRIPT_STATE"]
old-location: intl\script_state.htm
tech.root: Intl
ms.assetid: 4b1724f7-7773-42c0-9c19-fbded5aef14e
ms.date: 12/05/2018
ms.keywords: FALSE, SCRIPT_STATE, SCRIPT_STATE structure [Internationalization for Windows Applications], TRUE, _win32_SCRIPT_STATE_str, intl.script_state, usp10/SCRIPT_STATE
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
req.typenames: SCRIPT_STATE
req.redist: Internet Explorer 5 or later onWindows Me/98/95
ms.custom: 19H1
f1_keywords:
 - tag_SCRIPT_STATE
 - usp10/tag_SCRIPT_STATE
 - SCRIPT_STATE
 - usp10/SCRIPT_STATE
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
 - SCRIPT_STATE
---

# SCRIPT_STATE structure


## -description

Contains script state information.

## -struct-fields

### -field uBidiLevel

Embedding level associated with all characters in the associated run according to the Unicode bidirectional algorithm. When the application passes this structure to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>, this member should be initialized to 0 for a left-to-right base embedding level, or to 1 for a right-to-left base embedding level.

### -field fOverrideDirection

Initial override direction value indicating if the script uses an override level (LRO or RLO code in the string). Possible values are defined in the following table. For an override level, characters are laid out in one direction only, either left to right or right to left. No reordering of digits or strong characters of opposing direction takes place. Note that this value is reset by LRE, RLE, LRO or RLO codes in the string.

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
Use an override level that reflects the embedding level.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not use an override level that reflects the embedding level.

</td>
</tr>
</table>

### -field fInhibitSymSwap

Value indicating if the shaping engine bypasses mirroring of Unicode mirrored glyphs, for example, brackets. Possible values are defined in the following table. This member is set by Unicode character ISS, and cleared by ASS.

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
Bypass mirroring of Unicode mirrored glyphs.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not bypass mirroring of Unicode mirrored glyphs.

</td>
</tr>
</table>

### -field fCharShape

Not implemented. Value indicating if character codes in the Arabic Presentation Forms areas of Unicode should be shaped. Possible values are defined in the following table.

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
Shape character codes in the Arabic Presentation Forms areas of Unicode.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not shape character codes in the Arabic Presentation Forms areas of Unicode.

</td>
</tr>
</table>

### -field fDigitSubstitute

This member provides the same control over digit substitution behavior that might have been obtained in legacy implementations using the now-deprecated Unicode characters U+206E NATIONAL DIGIT SHAPES ("NADS") and U+206F NOMINAL DIGIT SHAPES ("NODS"). Possible values are defined in the following table.

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
Character codes U+0030 through U+0039 are substituted by national digits. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Character codes U+0030 through U+0039 are  not substituted by national digits. 

</td>
</tr>
</table>

### -field fInhibitLigate

Value indicating if ligatures are used in the shaping of Arabic or Hebrew characters. Possible values are defined in the following table. 

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
Do not use ligatures in the shaping of Arabic or Hebrew characters.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Use ligatures in the shaping of Arabic or Hebrew characters.

</td>
</tr>
</table>

### -field fDisplayZWG

Value indicating if nondisplayable control characters are shaped as representational glyphs for languages that need reordering or different glyph shapes, depending on the positions of the characters within a word. Possible values are defined in the following table. Typically, the characters are not displayed. They are shaped to the blank glyph and given a width of 0.
	 

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
Shape control characters as representational glyphs. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not shape control characters as representational glyphs. 

</td>
</tr>
</table>

### -field fArabicNumContext

Value indicating if prior strong characters are Arabic for the purposes of rule P0, as discussed in the Unicode Standard, version 2.0. Possible values are defined in the following table. This member should normally be set to <b>TRUE</b> before itemization of a right-to-left paragraph in an Arabic language, and to <b>FALSE</b> otherwise.

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
Consider prior strong characters to be Arabic for the purposes of rule P0.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not consider prior strong characters to be Arabic for the purposes of rule P0.

</td>
</tr>
</table>

### -field fGcpClusters

For <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> legacy support only. Value indicating how <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> should generate the array indicated by <i>pwLogClust</i>. Possible values are defined in the following table. This member affects only Arabic and Hebrew items.

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
Generate the array the same way as <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> does.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not generate the array the same way as <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> does.

</td>
</tr>
</table>

### -field fReserved

Reserved; always initialize to 0.

### -field fEngineReserved

Reserved; always initialize to 0.

## -remarks

This structure is used to initialize the Unicode algorithm state as an input to <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>. It is also used as a component of the analysis retrieved by <b>ScriptItemize</b>.

## -see-also

<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>