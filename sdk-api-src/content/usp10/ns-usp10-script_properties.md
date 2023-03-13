---
UID: NS:usp10.SCRIPT_PROPERTIES
title: SCRIPT_PROPERTIES (usp10.h)
description: Contains information about special processing for each script.
helpviewer_keywords: ["FALSE","SCRIPT_PROPERTIES","SCRIPT_PROPERTIES structure [Internationalization for Windows Applications]","TRUE","_win32_SCRIPT_PROPERTIES_str","intl.script_properties","usp10/SCRIPT_PROPERTIES"]
old-location: intl\script_properties.htm
tech.root: Intl
ms.assetid: 473c1265-1c2c-48f3-a852-c701bebcf9eb
ms.date: 12/05/2018
ms.keywords: FALSE, SCRIPT_PROPERTIES, SCRIPT_PROPERTIES structure [Internationalization for Windows Applications], TRUE, _win32_SCRIPT_PROPERTIES_str, intl.script_properties, usp10/SCRIPT_PROPERTIES
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
req.typenames: SCRIPT_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCRIPT_PROPERTIES
 - usp10/SCRIPT_PROPERTIES
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
 - SCRIPT_PROPERTIES
---

# SCRIPT_PROPERTIES structure


## -description

Contains information about special processing for each script.

## -struct-fields

### -field langid

<a href="/windows/desktop/Intl/language-identifiers">Language identifier</a> for the language associated with the script. When a script is used for many languages, this member represents a default language. For example, Western script is represented by LANG_ENGLISH although it is also used for French, German, and other European languages.

### -field fNumeric

Value indicating if a script contains only digits and the other characters used in writing numbers by the rules of the Unicode bidirectional algorithm. For example, currency symbols, the thousands separator, and the decimal point are classified as numeric when adjacent to or between digits. Possible values for this member are defined in the following table.

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
The script contains only digits and the other characters used in writing numbers by the rules of the Unicode bidirectional algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The script does not contain only digits and the other characters used in writing numbers by the rules of the Unicode bidirectional algorithm.

</td>
</tr>
</table>

### -field fComplex

Value indicating a complex script for a language that requires special shaping or layout. Possible values are defined in the following table. 

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
The script requires special shaping or layout.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The script contains no combining characters and requires no contextual shaping or reordering.

</td>
</tr>
</table>

### -field fNeedsWordBreaking

Value indicating the type of word break placement for a language. Possible values are defined in the following table. 

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
The language has word break placement that requires the application to call <a href="/windows/desktop/api/usp10/nf-usp10-scriptbreak">ScriptBreak</a> and that includes character positions marked by the <b>fWordStop</b> member in <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Word break placement is identified by scanning for characters marked by the <b>fWhiteSpace</b> member in <a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a>, or for glyphs marked by the value SCRIPT_JUSTIFY_BLANK or SCRIPT_JUSTIFY_ARABIC_BLANK for the <b>uJustification</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>.

</td>
</tr>
</table>

### -field fNeedsCaretInfo

Value indicating if a language, for example, Thai or Indian, restricts caret placement to cluster boundaries. Possible values are defined in the following table. To determine valid caret positions, the application inspects the <b>fCharStop</b> value in the logical attributes retrieved by <a href="/windows/desktop/api/usp10/nf-usp10-scriptbreak">ScriptBreak</a>, or compares adjacent values in the <i>pwLogClust</i> array retrieved by <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>.

<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/usp10/nf-usp10-scriptxtocp">ScriptXtoCP</a> and <a href="/windows/desktop/api/usp10/nf-usp10-scriptcptox">ScriptCPtoX</a> automatically apply caret placement restrictions.</div>
<div> </div>
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
The language restricts caret placement to cluster boundaries.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The language does not restrict caret placement to cluster boundaries.

</td>
</tr>
</table>

### -field bCharSet

Nominal character set associated with the script. During creation of a font suitable for displaying the script, this character set can be used as the value of the <b>lfCharSet</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a>.

For a new script having no character set defined, the application should typically set <b>bCharSet</b> to DEFAULT_CHARSET. See the description of member <b>fAmbiguousCharSet</b>.

### -field fControl

Value indicating if only control characters are used in the script. Possible values are defined in the following table. Note that every control character does not end up in a <a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a> structure.

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
Set only control characters in the script.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not set only control characters in the script.

</td>
</tr>
</table>

### -field fPrivateUseArea

Value indicating the use of a private use area, a special set of characters that is privately defined for the Unicode range U+E000 through U+F8FF. Possible values are defined in the following table. 

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
Use a private use area.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not use a private use area.

</td>
</tr>
</table>

### -field fNeedsCharacterJustify

Value indicating the handling of justification for the script by increasing all the spaces between letters, not just the spaces between words. Possible values are defined in the following table. When performing inter-character justification, Uniscribe inserts extra space only after glyphs marked with the SCRIPT_JUSTIFY_CHARACTER value for the <b>uJustification</b> member of <a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>.

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
Use character justification.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not use character justification.

</td>
</tr>
</table>

### -field fInvalidGlyph

Value indicating if <a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a> generates an invalid glyph for a script to represent invalid sequences. Possible values are defined in the following table. The application can obtain the glyph index of the invalid glyph for a particular font by calling <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontproperties">ScriptGetFontProperties</a>.

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
Generate an invalid glyph to represent invalid sequences.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not generate an invalid glyph to represent invalid sequences.

</td>
</tr>
</table>

### -field fInvalidLogAttr

Value indicating if <a href="/windows/desktop/api/usp10/nf-usp10-scriptbreak">ScriptBreak</a> marks invalid combinations for a script by setting <b>fInvalid</b> in the logical attributes buffer. Possible values are defined in the following table. 

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
Mark invalid combinations for the script.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not mark invalid combinations for the script.

</td>
</tr>
</table>

### -field fCDM

Value indicating if a script contains an item that has been analyzed by <a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a> as including Combining Diacritical Marks (U+0300 through U+36F). Possible values are defined in the following table. 

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
The script contains an item that includes combining diacritical marks.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The script does not contain an item that includes combining diacritical marks.

</td>
</tr>
</table>

### -field fAmbiguousCharSet

Value indicating if a script contains characters that are supported by more than one character set. Possible values are defined in the following table. 

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
The script contains characters that are supported by more than one character set. In this case, the <b>bCharSet</b> member of this structure should be ignored, and the <b>lfCharSet</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> should be set to DEFAULT_CHARSET. See the Remarks section for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The script does not contain characters that are supported by more than one character set.

</td>
</tr>
</table>

### -field fClusterSizeVaries

Value indicating if a script, such as Arabic, might use contextual shaping that causes a string to increase in size during removal of characters. Possible values are defined in the following table. 

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
Use a variable cluster size for contextual shaping.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not use a variable cluster size for contextual shaping.

</td>
</tr>
</table>

### -field fRejectInvalid

Value indicating if a script, for example, Thai, should reject invalid sequences that conventionally cause an editor program, such as Notepad, to beep and ignore keystrokes. Possible values are defined in the following table. 

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
Reject invalid sequences.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not reject invalid sequences.

</td>
</tr>
</table>

## -remarks

This structure is filled by the <a href="/windows/desktop/api/usp10/nf-usp10-scriptgetproperties">ScriptGetProperties</a> function.

Many Uniscribe scripts do not correspond directly to 8-bit character sets. When some of the characters in a script are supported by more than one character set, the <b>fAmbiguousCharSet</b> member is set. The application should do further processing to determine the character set to use when requesting a font suitable for the run. For example, it might determine that the run consists of multiple languages and split the run so that a different font is used for each language.

The application uses the following code during initialization to get a pointer to the <b>SCRIPT_PROPERTIES</b>  array.


```cpp
const SCRIPT_PROPERTIES **ppScriptProperties; // Array of pointers  
                                              // to properties 
int iMaxScript;
HRESULT hr;

hr = ScriptGetProperties(&ppScriptProperties, &iMaxScript);

```


Then the application can inspect the properties of the script of an item as shown in the next example.


```cpp
hr = ScriptItemize(pwcInChars, cInChars, cMaxItems, psControl, psState, pItems, pcItems);
//...
if (ppScriptProperties[pItems[iItem].a.eScript]->fNeedsCaretInfo) 
    {
        // Use ScriptBreak to restrict the caret from entering clusters (for example). 
    }

```

## -see-also

<a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_control">SCRIPT_CONTROL</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_logattr">SCRIPT_LOGATTR</a>



<a href="/windows/win32/api/usp10/ns-usp10-script_visattr">SCRIPT_VISATTR</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptbreak">ScriptBreak</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptcptox">ScriptCPtoX</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptgetfontproperties">ScriptGetFontProperties</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptgetproperties">ScriptGetProperties</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptitemize">ScriptItemize</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptshape">ScriptShape</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptxtocp">ScriptXtoCP</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>

