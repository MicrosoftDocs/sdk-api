---
UID: NS:wincon._CONSOLE_SELECTION_INFO
title: "_CONSOLE_SELECTION_INFO"
author: windows-driver-content
description: Contains information for a console selection.
old-location: consoles\console_selection_info_str.htm
old-project: consoles
ms.assetid: 9530b249-8db4-4516-9cc8-2b452c6751f9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCONSOLE_SELECTION_INFO, CONSOLE_MOUSE_DOWN, CONSOLE_MOUSE_SELECTION, CONSOLE_NO_SELECTION, CONSOLE_SELECTION_INFO, CONSOLE_SELECTION_INFO structure [Consoles], CONSOLE_SELECTION_IN_PROGRESS, CONSOLE_SELECTION_NOT_EMPTY, PCONSOLE_SELECTION_INFO, PCONSOLE_SELECTION_INFO structure pointer [Consoles], _CONSOLE_SELECTION_INFO, _win32_console_selection_info_str, base.console_selection_info_str, consoles.console_selection_info_str, wincon/CONSOLE_SELECTION_INFO, wincon/PCONSOLE_SELECTION_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: CONSOLE_SELECTION_INFO, *PCONSOLE_SELECTION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	CONSOLE_SELECTION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CONSOLE_SELECTION_INFO structure


## -description


Contains information for a console selection.


## -struct-fields




### -field dwFlags

The selection indicator. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_MOUSE_DOWN"></a><a id="console_mouse_down"></a><dl>
<dt><b>CONSOLE_MOUSE_DOWN</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Mouse is down

</td>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_MOUSE_SELECTION"></a><a id="console_mouse_selection"></a><dl>
<dt><b>CONSOLE_MOUSE_SELECTION</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Selecting with the mouse

</td>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_NO_SELECTION"></a><a id="console_no_selection"></a><dl>
<dt><b>CONSOLE_NO_SELECTION</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
No selection

</td>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_SELECTION_IN_PROGRESS"></a><a id="console_selection_in_progress"></a><dl>
<dt><b>CONSOLE_SELECTION_IN_PROGRESS</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Selection has begun

</td>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_SELECTION_NOT_EMPTY"></a><a id="console_selection_not_empty"></a><dl>
<dt><b>CONSOLE_SELECTION_NOT_EMPTY</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Selection rectangle is not empty

</td>
</tr>
</table>
 


### -field dwSelectionAnchor

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that specifies the selection anchor, in characters.


### -field srSelection

A 
<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a> structure that specifies the selection rectangle.


## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/912efe9d-75dd-43bd-8dca-08671b5ed79c">GetConsoleSelectionInfo</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>
 

 

