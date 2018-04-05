---
UID: NS:wincon._CONSOLE_FONT_INFOEX
title: "_CONSOLE_FONT_INFOEX"
author: windows-driver-content
description: Contains extended information for a console font.
old-location: consoles\console_font_infoex.htm
old-project: consoles
ms.assetid: e9a087e1-264d-4d48-8adb-771a0e35b511
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCONSOLE_FONT_INFOEX, CONSOLE_FONT_INFOEX, CONSOLE_FONT_INFOEX structure [Consoles], PCONSOLE_FONT_INFOEX, PCONSOLE_FONT_INFOEX structure pointer [Consoles], _CONSOLE_FONT_INFOEX, base.console_font_infoex, consoles.console_font_infoex, wincon/CONSOLE_FONT_INFOEX, wincon/PCONSOLE_FONT_INFOEX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CONSOLE_FONT_INFOEX, *PCONSOLE_FONT_INFOEX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	CONSOLE_FONT_INFOEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CONSOLE_FONT_INFOEX structure


## -description


Contains extended information for a console font.


## -struct-fields




### -field cbSize

The size of this structure, in bytes.


### -field nFont

The index of the font in the system's console font table.


### -field dwFontSize

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that contains the width and height of each character in the font, in logical units. The <b>X</b> member contains the width, while the <b>Y</b> member contains the height.


### -field FontFamily

The font pitch and  family. For information about the possible values for this member, see the description of the <b>tmPitchAndFamily</b> member of the <a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRIC</a> structure.


### -field FontWeight

The font weight. The weight can range from 100 to 1000, in multiples of 100. For example, the normal weight is 400, while 700 is bold.


### -field FaceName

The name of the typeface (such as Courier or Arial).


## -remarks



To obtain the size of the font, pass the font index to the 
<a href="https://msdn.microsoft.com/51b1f58d-b3fb-4e09-8398-671b3959bb01">GetConsoleFontSize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/97d8e730-4110-4be5-b099-0acc1b6f8eb5">GetCurrentConsoleFontEx</a>
 

 

