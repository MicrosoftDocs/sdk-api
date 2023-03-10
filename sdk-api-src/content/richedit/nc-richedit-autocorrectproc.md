---
UID: NC:richedit.AutoCorrectProc
title: AutoCorrectProc (richedit.h)
description: The AutoCorrectProc function is an application-defined callback function that is used with the EM_SETAUTOCORRECTPROC message.
helpviewer_keywords: ["AutoCorrectProc","AutoCorrectProc callback","AutoCorrectProc callback function [Windows Controls]","controls.autocorrectproc","richedit/AutoCorrectProc"]
old-location: controls\autocorrectproc.htm
tech.root: Controls
ms.assetid: 36EF880D-F6A9-434A-820B-17E663357573
ms.date: 12/05/2018
ms.keywords: AutoCorrectProc, AutoCorrectProc callback, AutoCorrectProc callback function [Windows Controls], controls.autocorrectproc, richedit/AutoCorrectProc
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AutoCorrectProc
 - richedit/AutoCorrectProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Richedit.h
api_name:
 - AutoCorrectProc
---

# AutoCorrectProc callback function


## -description

The <i>AutoCorrectProc</i> function is an 
    application-defined  callback function that is used with the 
    <a href="/windows/desktop/Controls/em-setautocorrectproc">EM_SETAUTOCORRECTPROC</a> message.

<i>AutoCorrectProc</i> is a placeholder for the 
    application-defined function name. It provides application-defined automatic error correction for text entered 
    into a rich edit control.

## -parameters

### -param langid

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LANGID</a></b>

Language ID that identifies the autocorrect file to use for automatic correcting.

### -param pszBefore

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">WCHAR</a>*</b>

Autocorrect candidate string.

### -param pszAfter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WCHAR</a>*</b>

Resulting autocorrect string, if the return value is not <b>ATP_NOCHANGE</b>.

### -param cchAfter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Count of characters in <i>pszAfter</i>.

### -param pcchReplaced

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

Count of trailing characters in <i>pszBefore</i> to replace with <i>pszAfter</i>.

## -returns

Type: <b>int</b>

Returns one or more of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ATP_NOCHANGE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No change.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ATP_CHANGE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Change but don’t replace most delimiters, and don’t replace a span of unchanged trailing characters (preserves their formatting).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ATP_NODELIMITER</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Change but don’t replace a span of unchanged trailing characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ATP_REPLACEALLTEXT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Replace trailing characters even if they are not changed (uses the same formatting for the entire replacement string). 


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Controls/em-callautocorrectproc">EM_CALLAUTOCORRECTPROC</a>



<a href="/windows/desktop/Controls/em-getautocorrectproc">EM_GETAUTOCORRECTPROC</a>



<a href="/windows/desktop/Controls/em-setautocorrectproc">EM_SETAUTOCORRECTPROC</a>
