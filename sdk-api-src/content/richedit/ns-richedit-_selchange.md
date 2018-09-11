---
UID: NS:richedit._selchange
title: "_selchange"
author: windows-sdk-content
description: Contains information associated with an EN_SELCHANGE notification code. A rich edit control sends this notification to its parent window when the current selection changes.
old-location: controls\SELCHANGE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\selchange.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SELCHANGE, SELCHANGE structure [Windows Controls], SEL_MULTICHAR, SEL_MULTIOBJECT, SEL_OBJECT, SEL_TEXT, _selchange, _win32_SELCHANGE_str, _win32_SELCHANGE_str_cpp, controls.SELCHANGE, controls._win32_SELCHANGE_str, richedit/SELCHANGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: SELCHANGE
req.redist: 
---

# _selchange structure


## -description


Contains information associated with an <a href="https://msdn.microsoft.com/en-us/library/Bb787987(v=VS.85).aspx">EN_SELCHANGE</a> notification code. A rich edit control sends this notification to its parent window when the current selection changes.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

Notification header. 


### -field chrg

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a></b>

New selection range. 


### -field seltyp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WORD</a></b>

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




<a href="https://msdn.microsoft.com/en-us/library/Bb787987(v=VS.85).aspx">EN_SELCHANGE</a>
 

 

