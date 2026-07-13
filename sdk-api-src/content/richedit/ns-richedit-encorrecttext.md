---
UID: NS:richedit._encorrecttext
title: ENCORRECTTEXT (richedit.h)
description: Contains information about the selected text to be corrected.
helpviewer_keywords: ["ENCORRECTTEXT","ENCORRECTTEXT structure [Windows Controls]","SEL_MULTICHAR","SEL_MULTIOBJECT","SEL_OBJECT","SEL_TEXT","_win32_ENCORRECTTEXT_str","_win32_ENCORRECTTEXT_str_cpp","controls.ENCORRECTTEXT","controls._win32_ENCORRECTTEXT_str","richedit/ENCORRECTTEXT"]
old-location: controls\ENCORRECTTEXT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\encorrecttext.htm
ms.date: 12/05/2018
ms.keywords: ENCORRECTTEXT, ENCORRECTTEXT structure [Windows Controls], SEL_MULTICHAR, SEL_MULTIOBJECT, SEL_OBJECT, SEL_TEXT, _win32_ENCORRECTTEXT_str, _win32_ENCORRECTTEXT_str_cpp, controls.ENCORRECTTEXT, controls._win32_ENCORRECTTEXT_str, richedit/ENCORRECTTEXT
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
req.typenames: ENCORRECTTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _encorrecttext
 - richedit/_encorrecttext
 - ENCORRECTTEXT
 - richedit/ENCORRECTTEXT
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
 - ENCORRECTTEXT
---

# ENCORRECTTEXT structure


## -description

Contains information about the selected text to be corrected.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure. The <b>code</b> member of this structure identifies the notification code being sent.

### -field chrg

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

A <a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a> structure that specifies the range of selected characters.

### -field seltyp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Value specifying the contents of the new selection. This member is SEL_EMPTY if the selection is empty or one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEL_TEXT"></a><a id="sel_text"></a><dl>
<dt><b>SEL_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The new selection contains text.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_OBJECT"></a><a id="sel_object"></a><dl>
<dt><b>SEL_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The new selection contains at least one COM object.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_MULTICHAR"></a><a id="sel_multichar"></a><dl>
<dt><b>SEL_MULTICHAR</b></dt>
</dl>
</td>
<td width="60%">
The new selection contains more than one character of text.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_MULTIOBJECT"></a><a id="sel_multiobject"></a><dl>
<dt><b>SEL_MULTIOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The new selection contains more than one COM object.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/controls/en-correcttext">EN_CORRECTTEXT</a>
