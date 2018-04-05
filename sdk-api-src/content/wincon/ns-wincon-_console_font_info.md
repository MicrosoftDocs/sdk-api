---
UID: NS:wincon._CONSOLE_FONT_INFO
title: "_CONSOLE_FONT_INFO"
author: windows-driver-content
description: Contains information for a console font.
old-location: consoles\console_font_info_str.htm
old-project: consoles
ms.assetid: 380b8183-1964-46f2-a511-01f39f21f5c5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCONSOLE_FONT_INFO, CONSOLE_FONT_INFO, CONSOLE_FONT_INFO structure [Consoles], PCONSOLE_FONT_INFO, PCONSOLE_FONT_INFO structure pointer [Consoles], _CONSOLE_FONT_INFO, _win32_console_font_info_str, base.console_font_info_str, consoles.console_font_info_str, wincon/CONSOLE_FONT_INFO, wincon/PCONSOLE_FONT_INFO"
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
req.typenames: CONSOLE_FONT_INFO, *PCONSOLE_FONT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	CONSOLE_FONT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CONSOLE_FONT_INFO structure


## -description


Contains information for a console font.


## -struct-fields




### -field nFont

The index of the font in the system's console font table.


### -field dwFontSize

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that contains the width and height of each character in the font, in logical units. The <b>X</b> member contains the width, while the <b>Y</b> member contains the height.


## -remarks



To obtain the size of the font, pass the font index to the 
<a href="https://msdn.microsoft.com/51b1f58d-b3fb-4e09-8398-671b3959bb01">GetConsoleFontSize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/347508ea-5c15-4568-b99f-1e7f5cdac8c1">GetCurrentConsoleFont</a>
 

 

