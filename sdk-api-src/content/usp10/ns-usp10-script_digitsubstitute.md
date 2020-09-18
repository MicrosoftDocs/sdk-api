---
UID: NS:usp10.tag_SCRIPT_DIGITSUBSTITUTE
title: SCRIPT_DIGITSUBSTITUTE (usp10.h)
description: Contains native digit and digit substitution settings.
helpviewer_keywords: ["SCRIPT_DIGITSUBSTITUTE","SCRIPT_DIGITSUBSTITUTE structure [Internationalization for Windows Applications]","SCRIPT_DIGITSUBSTITUTE_CONTEXT","SCRIPT_DIGITSUBSTITUTE_NATIONAL","SCRIPT_DIGITSUBSTITUTE_NONE","SCRIPT_DIGITSUBSTITUTE_TRADITIONAL","_win32_SCRIPT_DIGITSUBSTITUTE_str","intl.script_digitsubstitute","usp10/SCRIPT_DIGITSUBSTITUTE"]
old-location: intl\script_digitsubstitute.htm
tech.root: Intl
ms.assetid: e96bf8b4-7456-4e16-a623-48320104dd66
ms.date: 12/05/2018
ms.keywords: SCRIPT_DIGITSUBSTITUTE, SCRIPT_DIGITSUBSTITUTE structure [Internationalization for Windows Applications], SCRIPT_DIGITSUBSTITUTE_CONTEXT, SCRIPT_DIGITSUBSTITUTE_NATIONAL, SCRIPT_DIGITSUBSTITUTE_NONE, SCRIPT_DIGITSUBSTITUTE_TRADITIONAL, _win32_SCRIPT_DIGITSUBSTITUTE_str, intl.script_digitsubstitute, usp10/SCRIPT_DIGITSUBSTITUTE
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
req.typenames: SCRIPT_DIGITSUBSTITUTE
req.redist: Internet Explorer 5 or later onWindows Me/98/95
ms.custom: 19H1
f1_keywords:
 - tag_SCRIPT_DIGITSUBSTITUTE
 - usp10/tag_SCRIPT_DIGITSUBSTITUTE
 - SCRIPT_DIGITSUBSTITUTE
 - usp10/SCRIPT_DIGITSUBSTITUTE
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
 - SCRIPT_DIGITSUBSTITUTE
---

# SCRIPT_DIGITSUBSTITUTE structure


## -description

Contains native digit and digit substitution settings.

## -struct-fields

### -field NationalDigitLanguage

Language for native substitution.

### -field TraditionalDigitLanguage

Language for traditional substitution.

### -field DigitSubstitute

Substitution type. This member is normally set by <a href="/windows/desktop/api/usp10/nf-usp10-scriptrecorddigitsubstitution">ScriptRecordDigitSubstitution</a>. However, it can also have any of the values defined in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCRIPT_DIGITSUBSTITUTE_CONTEXT_"></a><a id="script_digitsubstitute_context_"></a><dl>
<dt><b>SCRIPT_DIGITSUBSTITUTE_CONTEXT </b></dt>
</dl>
</td>
<td width="60%">
Substitute digits U+0030 to U+0039 using the language of the prior letters. If there are no prior letters, substitute digits using the <b>TraditionalDigitLanguage</b> member. This member is normally set to the primary language of the locale passed to <a href="/windows/desktop/api/usp10/nf-usp10-scriptrecorddigitsubstitution">ScriptRecordDigitSubstitution</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCRIPT_DIGITSUBSTITUTE_NATIONAL"></a><a id="script_digitsubstitute_national"></a><dl>
<dt><b>SCRIPT_DIGITSUBSTITUTE_NATIONAL</b></dt>
</dl>
</td>
<td width="60%">
Substitute digits U+0030 to U+0039 using the <b>NationalDigitLanguage</b> member. This member is normally set to the national digits retrieved for the constant <a href="/windows/desktop/Intl/locale-snative-constants">LOCALE_SNATIVEDIGITS</a> by <a href="/windows/desktop/api/usp10/nf-usp10-scriptrecorddigitsubstitution">ScriptRecordDigitSubstitution</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCRIPT_DIGITSUBSTITUTE_NONE"></a><a id="script_digitsubstitute_none"></a><dl>
<dt><b>SCRIPT_DIGITSUBSTITUTE_NONE</b></dt>
</dl>
</td>
<td width="60%">
Do not substitute digits. Display Unicode values U+0030 to U+0039 with European numerals.

</td>
</tr>
<tr>
<td width="40%"><a id="SCRIPT_DIGITSUBSTITUTE_TRADITIONAL"></a><a id="script_digitsubstitute_traditional"></a><dl>
<dt><b>SCRIPT_DIGITSUBSTITUTE_TRADITIONAL</b></dt>
</dl>
</td>
<td width="60%">
Substitute digits U+0030 to U+0039 using the <b>TraditionalDigitLanguage</b> member. This member is normally set to the primary language of the locale passed to <a href="/windows/desktop/api/usp10/nf-usp10-scriptrecorddigitsubstitution">ScriptRecordDigitSubstitution</a>.

</td>
</tr>
</table>

### -field dwReserved

Reserved; initialize to 0.

## -see-also

<a href="/windows/desktop/Intl/digit-shapes">Digit Shapes</a>



<a href="/windows/desktop/api/usp10/nf-usp10-scriptrecorddigitsubstitution">ScriptRecordDigitSubstitution</a>



<a href="/windows/desktop/Intl/uniscribe">Uniscribe</a>



<a href="/windows/desktop/Intl/uniscribe-structures">Uniscribe Structures</a>