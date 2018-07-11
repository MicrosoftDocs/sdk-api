---
UID: NS:richedit._settextex
title: "_settextex"
author: windows-sdk-content
description: Specifies which code page (if any) to use in setting text, whether the text replaces all the text in the control or just the selection, and whether the undo state is to be preserved. This structure is used with the EM_SETTEXTEX message.
old-location: controls\SETTEXTEX.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\settextex.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: SETTEXTEX, SETTEXTEX structure [Windows Controls], ST_DEFAULT, ST_KEEPUNDO, ST_NEWCHARS, ST_SELECTION, ST_UNICODE, _settextex, _win32_SETTEXTEX_str, _win32_SETTEXTEX_str_cpp, controls.SETTEXTEX, controls._win32_SETTEXTEX_str, richedit/SETTEXTEX
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
tech.root: 
req.typenames: SETTEXTEX
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - SETTEXTEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _settextex structure


## -description


Specifies which code page (if any) to use in setting text, whether the text replaces all the text in the control or just the selection, and whether the undo state is to be preserved. This structure is used with the <a href="https://msdn.microsoft.com/1ba9e4c0-7870-4057-8a8b-d0e6577349ac">EM_SETTEXTEX</a> message. 


## -struct-fields




### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Option flags. It can be any reasonable combination of the following flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ST_DEFAULT"></a><a id="st_default"></a><dl>
<dt><b>ST_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Deletes the undo stack, discards rich-text formatting, replaces all text.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_KEEPUNDO"></a><a id="st_keepundo"></a><dl>
<dt><b>ST_KEEPUNDO</b></dt>
</dl>
</td>
<td width="60%">
Keeps the undo stack.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_SELECTION"></a><a id="st_selection"></a><dl>
<dt><b>ST_SELECTION</b></dt>
</dl>
</td>
<td width="60%">
Replaces selection and keeps rich-text formatting.

</td>
</tr>
<tr>
<td width="40%"><a id="ST_NEWCHARS"></a><a id="st_newchars"></a><dl>
<dt><b>ST_NEWCHARS</b></dt>
</dl>
</td>
<td width="60%">
Act as if new characters are being entered. 


</td>
</tr>
<tr>
<td width="40%"><a id="ST_UNICODE"></a><a id="st_unicode"></a><dl>
<dt><b>ST_UNICODE</b></dt>
</dl>
</td>
<td width="60%">
The text is UTF-16 
(the <b>WCHAR</b> data type).

</td>
</tr>
</table>
 


### -field codepage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The code page used to translate the text to Unicode. If <b>codepage</b> is 1200 (Unicode code page), no translation is done. If <b>codepage</b> is CP_ACP, the system code page is used. 


## -see-also




<a href="https://msdn.microsoft.com/1ba9e4c0-7870-4057-8a8b-d0e6577349ac">EM_SETTEXTEX</a>
 

 

