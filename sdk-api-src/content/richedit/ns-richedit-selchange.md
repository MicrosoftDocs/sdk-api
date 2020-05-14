---
UID: NS:richedit._selchange
title: SELCHANGE (richedit.h)
description: Contains information associated with an EN_SELCHANGE notification code. A rich edit control sends this notification to its parent window when the current selection changes.helpviewer_keywords: ["SELCHANGE","SELCHANGE structure [Windows Controls]","SEL_MULTICHAR","SEL_MULTIOBJECT","SEL_OBJECT","SEL_TEXT","_win32_SELCHANGE_str","_win32_SELCHANGE_str_cpp","controls.SELCHANGE","controls._win32_SELCHANGE_str","richedit/SELCHANGE"]
old-location: controls\SELCHANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\selchange.htm
ms.date: 12/05/2018
ms.keywords: SELCHANGE, SELCHANGE structure [Windows Controls], SEL_MULTICHAR, SEL_MULTIOBJECT, SEL_OBJECT, SEL_TEXT, _win32_SELCHANGE_str, _win32_SELCHANGE_str_cpp, controls.SELCHANGE, controls._win32_SELCHANGE_str, richedit/SELCHANGE
f1_keywords:
- richedit/SELCHANGE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Richedit.h
api_name:
- SELCHANGE
targetos: Windows
req.typenames: SELCHANGE
req.redist: 
ms.custom: 19H1
---

# SELCHANGE structure


## -description


Contains information associated with an <a href="https://msdn.microsoft.com/53d47b53-a73c-4652-889c-2374f8e99382">EN_SELCHANGE</a> notification code. A rich edit control sends this notification to its parent window when the current selection changes.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

Notification header. 


### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

New selection range. 


### -field seltyp

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">WORD</a></b>

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
Text.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_OBJECT"></a><a id="sel_object"></a><dl>
<dt><b>SEL_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
At least one COM object.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_MULTICHAR"></a><a id="sel_multichar"></a><dl>
<dt><b>SEL_MULTICHAR</b></dt>
</dl>
</td>
<td width="60%">
More than one character of text.

</td>
</tr>
<tr>
<td width="40%"><a id="SEL_MULTIOBJECT"></a><a id="sel_multiobject"></a><dl>
<dt><b>SEL_MULTIOBJECT</b></dt>
</dl>
</td>
<td width="60%">
More than one COM object.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/53d47b53-a73c-4652-889c-2374f8e99382">EN_SELCHANGE</a>
 

 

