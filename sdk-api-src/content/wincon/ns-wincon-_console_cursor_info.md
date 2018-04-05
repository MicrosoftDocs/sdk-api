---
UID: NS:wincon._CONSOLE_CURSOR_INFO
title: "_CONSOLE_CURSOR_INFO"
author: windows-driver-content
description: Contains information about the console cursor.
old-location: consoles\console_cursor_info_str.htm
old-project: consoles
ms.assetid: 0e71ce8c-e008-4bd7-922e-c44484b425ef
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCONSOLE_CURSOR_INFO, CONSOLE_CURSOR_INFO, CONSOLE_CURSOR_INFO structure [Consoles], PCONSOLE_CURSOR_INFO, PCONSOLE_CURSOR_INFO structure pointer [Consoles], _CONSOLE_CURSOR_INFO, _win32_console_cursor_info_str, base.console_cursor_info_str, consoles.console_cursor_info_str, wincon/CONSOLE_CURSOR_INFO, wincon/PCONSOLE_CURSOR_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
req.include-header: Windows.h
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
req.typenames: CONSOLE_CURSOR_INFO, *PCONSOLE_CURSOR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	CONSOLE_CURSOR_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CONSOLE_CURSOR_INFO structure


## -description


Contains information about the console cursor.


## -struct-fields




### -field dwSize

The percentage of the character cell that is filled by the cursor. This value is between 1 and 100. The cursor appearance varies, ranging from completely filling the cell to showing up as a horizontal line at the bottom of the cell.

<div class="alert"><b>Note</b>  While the <b>dwSize</b> value is normally between 1 and 100, under some circumstances a value outside of that range might be returned. For example, if <b>CursorSize</b> is set to 0 in the registry, the <b>dwSize</b> value returned would be 0. </div>
<div> </div>

### -field bVisible

The visibility of the cursor. If the cursor is visible, this member is <b>TRUE</b>.


## -see-also




<a href="https://msdn.microsoft.com/6200577d-8d84-46bd-9330-d0b6cbbb3e52">GetConsoleCursorInfo</a>



<a href="https://msdn.microsoft.com/c98cbffb-18de-41e8-bba7-5fb46a0c5d25">SetConsoleCursorInfo</a>
 

 

