---
UID: NS:richedit._gettextex
title: GETTEXTEX (richedit.h)
description: Contains information used in getting text from a rich edit control. This structure used with the EM_GETTEXTEX message.
helpviewer_keywords: ["GETTEXTEX","GETTEXTEX structure [Windows Controls]","GT_DEFAULT","GT_NOHIDDENTEXT","GT_RAWTEXT","GT_SELECTION","GT_USECRLF","_win32_GETTEXTEX_str","_win32_GETTEXTEX_str_cpp","controls.GETTEXTEX","controls._win32_GETTEXTEX_str","richedit/GETTEXTEX"]
old-location: controls\GETTEXTEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\gettextex.htm
ms.date: 12/05/2018
ms.keywords: GETTEXTEX, GETTEXTEX structure [Windows Controls], GT_DEFAULT, GT_NOHIDDENTEXT, GT_RAWTEXT, GT_SELECTION, GT_USECRLF, _win32_GETTEXTEX_str, _win32_GETTEXTEX_str_cpp, controls.GETTEXTEX, controls._win32_GETTEXTEX_str, richedit/GETTEXTEX
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: GETTEXTEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _gettextex
 - richedit/_gettextex
 - GETTEXTEX
 - richedit/GETTEXTEX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - GETTEXTEX
---

# GETTEXTEX structure


## -description

Contains information used in getting text from a rich edit control. This structure used with the <a href="/windows/desktop/Controls/em-gettextex">EM_GETTEXTEX</a> message.

## -struct-fields

### -field cb

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The size, in bytes, of the buffer used to store the retrieved text.

### -field flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Value specifying a text operation. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GT_DEFAULT"></a><a id="gt_default"></a><dl>
<dt><b>GT_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
All text is retrieved according to the following criteria: 

<ul>
<li>Carriage returns (U+000D) are not translated into CRLF (U+000D U+000A).</li>
<li>Table and math-object structure characters are removed (see <b>GT_RAWTEXT</b>).</li>
<li>Hidden text is included. </li>
<li>List numbers are not included. 
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="GT_NOHIDDENTEXT"></a><a id="gt_nohiddentext"></a><dl>
<dt><b>GT_NOHIDDENTEXT</b></dt>
</dl>
</td>
<td width="60%">
 Hidden text is not included in the retrieved text. 


</td>
</tr>
<tr>
<td width="40%"><a id="GT_RAWTEXT"></a><a id="gt_rawtext"></a><dl>
<dt><b>GT_RAWTEXT</b></dt>
</dl>
</td>
<td width="60%">
Text is retrieved exactly as it appears in memory. This includes special structure characters for table row and cell delimiters (see Remarks for <a href="/windows/desktop/Controls/em-inserttable">EM_INSERTTABLE</a>) as well as math object delimiters (start delimiter U+FDD0, argument delimiter U+FDEE, and end delimiter U+FDDF) and object markers (U+FFFC). This maintains character-position alignment between the retrieved text and the text in memory. 


</td>
</tr>
<tr>
<td width="40%"><a id="GT_SELECTION"></a><a id="gt_selection"></a><dl>
<dt><b>GT_SELECTION</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the text for the current selection.

</td>
</tr>
<tr>
<td width="40%"><a id="GT_USECRLF"></a><a id="gt_usecrlf"></a><dl>
<dt><b>GT_USECRLF</b></dt>
</dl>
</td>
<td width="60%">
When copying text, translate each CR into a CR/LF.

</td>
</tr>
</table>

### -field codepage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Code page used in the translation. It is <b>CP_ACP</b> for ANSI code page and 1200 for Unicode.

### -field lpDefaultChar

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The character used if a wide character cannot be represented in the specified code page. It is used only if the code page is <b>not</b> 1200 (Unicode). If this member is <b>NULL</b>, a system default value is used.

### -field lpUsedDefChar

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPBOOL</a></b>

A flag that indicates whether the default character (<b>lpDefaultChar</b>) was used. This member is used only if the code page is not 1200 or <b>CP_UTF8</b> (Unicode). The flag is <b>TRUE</b> if one or more wide characters in the source string cannot be represented in the specified code page. Otherwise, the flag is <b>FALSE</b>. This member can be NULL.

## -remarks

The <a href="/windows/desktop/Controls/em-gettextex">EM_GETTEXTEX</a> message is faster when both <b>lpDefaultChar</b> and <b>lpUsedDefChar</b> are <b>NULL</b>.

## -see-also

<a href="/windows/desktop/Controls/em-gettextex">EM_GETTEXTEX</a>