---
UID: NS:richedit._gettextlengthex
title: GETTEXTLENGTHEX (richedit.h)
description: Contains information about how the text length of a rich edit control should be calculated. This structure is passed in the wParam in the EM_GETTEXTLENGTHEX message.
helpviewer_keywords: ["GETTEXTLENGTHEX","GETTEXTLENGTHEX structure [Windows Controls]","GTL_CLOSE","GTL_DEFAULT","GTL_NUMBYTES","GTL_NUMCHARS","GTL_PRECISE","GTL_USECRLF","_win32_GETTEXTLENGTHEX_str","_win32_GETTEXTLENGTHEX_str_cpp","controls.GETTEXTLENGTHEX","controls._win32_GETTEXTLENGTHEX_str","richedit/GETTEXTLENGTHEX"]
old-location: controls\GETTEXTLENGTHEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\gettextlengthex.htm
ms.date: 12/05/2018
ms.keywords: GETTEXTLENGTHEX, GETTEXTLENGTHEX structure [Windows Controls], GTL_CLOSE, GTL_DEFAULT, GTL_NUMBYTES, GTL_NUMCHARS, GTL_PRECISE, GTL_USECRLF, _win32_GETTEXTLENGTHEX_str, _win32_GETTEXTLENGTHEX_str_cpp, controls.GETTEXTLENGTHEX, controls._win32_GETTEXTLENGTHEX_str, richedit/GETTEXTLENGTHEX
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
req.typenames: GETTEXTLENGTHEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _gettextlengthex
 - richedit/_gettextlengthex
 - GETTEXTLENGTHEX
 - richedit/GETTEXTLENGTHEX
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
 - GETTEXTLENGTHEX
---

# GETTEXTLENGTHEX structure


## -description

Contains information about how the text length of a rich edit control should be calculated. This structure is passed in the <b>wParam</b> in the <a href="/windows/win32/controls/em-gettextlengthex">EM_GETTEXTLENGTHEX</a> message.

## -struct-fields

### -field flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Value specifying the method to be used in determining the text length. This member can be one or more of the following values (some values are mutually exclusive). 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GTL_DEFAULT"></a><a id="gtl_default"></a><dl>
<dt><b>GTL_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of characters. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_USECRLF"></a><a id="gtl_usecrlf"></a><dl>
<dt><b>GTL_USECRLF</b></dt>
</dl>
</td>
<td width="60%">
Computes the answer by using CR/LFs at the end of paragraphs.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_PRECISE"></a><a id="gtl_precise"></a><dl>
<dt><b>GTL_PRECISE</b></dt>
</dl>
</td>
<td width="60%">
Computes a precise answer. This approach could necessitate a conversion and thereby take longer. This flag cannot be used with the GTL_CLOSE flag. E_INVALIDARG will be returned if both are used.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_CLOSE"></a><a id="gtl_close"></a><dl>
<dt><b>GTL_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
Computes an approximate (close) answer. It is obtained quickly and can be used to set the buffer size. This flag cannot be used with the GTL_PRECISE flag. E_INVALIDARG will be returned if both are used.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_NUMCHARS"></a><a id="gtl_numchars"></a><dl>
<dt><b>GTL_NUMCHARS</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of characters. This flag cannot be used with the GTL_NUMBYTES flag. E_INVALIDARG will be returned if both are used.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_NUMBYTES"></a><a id="gtl_numbytes"></a><dl>
<dt><b>GTL_NUMBYTES</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of bytes. This flag cannot be used with the GTL_NUMCHARS flag. E_INVALIDARG will be returned if both are used.

</td>
</tr>
</table>

### -field codepage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Code page used in the translation. It is CP_ACP for ANSI Code Page and 1200 for Unicode.

## -see-also

<a href="/windows/win32/controls/em-gettextlengthex">EM_GETTEXTLENGTHEX</a>