---
UID: NS:usp10.tag_SCRIPT_CONTROL
title: SCRIPT_CONTROL (usp10.h)
description: Contains script control flags for several Uniscribe functions, for example, ScriptItemize.
helpviewer_keywords: ["FALSE","SCRIPT_CONTROL","SCRIPT_CONTROL structure [Internationalization for Windows Applications]","TRUE","_win32_SCRIPT_CONTROL_str","intl.script_control","usp10/SCRIPT_CONTROL"]
old-location: intl\script_control.htm
tech.root: Intl
ms.assetid: 4623f606-f67e-48ad-8c1d-d27da5ba556c
ms.date: 12/05/2018
ms.keywords: FALSE, SCRIPT_CONTROL, SCRIPT_CONTROL structure [Internationalization for Windows Applications], TRUE, _win32_SCRIPT_CONTROL_str, intl.script_control, usp10/SCRIPT_CONTROL
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
req.typenames: SCRIPT_CONTROL
req.redist: Internet Explorer 5 or later onWindows Me/98/95
ms.custom: 19H1
f1_keywords:
 - tag_SCRIPT_CONTROL
 - usp10/tag_SCRIPT_CONTROL
 - SCRIPT_CONTROL
 - usp10/SCRIPT_CONTROL
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
 - SCRIPT_CONTROL
---

# SCRIPT_CONTROL structure


## -description

Contains script control flags for several Uniscribe functions, for example, <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>.

## -struct-fields

### -field uDefaultLanguage

Primary <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> for the language to use when Unicode values are ambiguous. This value is used in numeric processing to select digit shape when the <b>fDigitSubstitute</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a> is set.

### -field fContextDigits

Value indicating how national digits are selected. Possible values are defined in the following table. 

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
Choose national digits according to the nearest previous strong text.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Choose national digits according to the value of the <b>uDefaultLanguage</b> member.

</td>
</tr>
</table>

### -field fInvertPreBoundDir

Value indicating if the initial context is set to the opposite of the base embedding level, or to the base embedding level itself. Possible values are defined in the following table. The application sets this member to indicate that text at the start of the string defaults to being laid out as if it follows a strong left-to-right character if the base <a href="/windows/desktop/Intl/uniscribe-glossary">embedding level</a> is 0, and as if it follows a strong right-to-left character if the base embedding level is 1. This member is used for <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> legacy support.

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
Change the initial context to the opposite of the base embedding level.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Set the initial context to the base embedding level.

</td>
</tr>
</table>

### -field fInvertPostBoundDir

Value indicating if the final context is set to the opposite of the base embedding level, or to the base embedding level itself. Possible values are defined in the following table. The application sets this member to indicate that text at the end of the string defaults to being laid out as if it precedes strong text of the same direction as the base embedding level. It is used for <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a> legacy support.

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
Change the final context to the opposite of the base embedding level.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Set the final context to the base embedding level.

</td>
</tr>
</table>

### -field fLinkStringBefore

Value indicating if the shaping engine shapes the first character of the string as if it joins with a previous character. Possible values are defined in the following table. 

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

### -field fLinkStringAfter

Value indicating if the shaping engine shapes the last character of the string as if it is joined to a subsequent character. Possible values are defined in the following table. 

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

### -field fNeutralOverride

Value indicating the treatment of all neutral characters in the string. Possible values are defined in the following table. 

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
Set neutral items to a strong direction, that is, right-to-left or left-to-right, depending on the current embedding level. This setting effectively locks the items in place, and reordering occurs only between neutrals.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not set neutral items to a strong direction.

</td>
</tr>
</table>

### -field fNumericOverride

Value indicating the treatment of all numeric characters in the string. Possible values are defined in the following table. 

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
Set numeric characters to a strong direction, that is, right-to-left or left-to-right, depending on the current embedding level. This setting effectively locks the items in place, and reordering occurs only between numeric characters.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not set numeric characters to a strong direction.

</td>
</tr>
</table>

### -field fLegacyBidiClass

Value indicating the handling for plus and minus characters by the shaping engine. Possible values are defined in the following table.

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
Treat the plus and minus characters as for legacy bidirectional classes in pre-Windows XP operating systems. In this case, the characters are treated as neutral characters, that is, with no implied direction, and the slash character is treated as a common separator.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Treat the plus and minus characters as for Windows XP and later. In this case, the characters are treated as European separators.

</td>
</tr>
</table>

### -field fMergeNeutralItems

Value specifying if the shaping engine should merge neutral characters into strong items when possible. Possible values are defined in the following table. 

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
Merge neutral characters into strong items.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not merge neutral characters into strong items.

</td>
</tr>
</table>

### -field fUseStandardBidi

Value specifying if the shaping engine should use the standard bidirectional matching pair algorithm. Possible values are defined in the following table. 

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
Skip the matching pair algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Use the matching pair algorithm.

</td>
</tr>
</table>

### -field fReserved

Reserved; always initialize to 0.

## -see-also

<a href="/windows/desktop/Intl/digit-shapes">Digit Shapes</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_state">SCRIPT_STATE</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>