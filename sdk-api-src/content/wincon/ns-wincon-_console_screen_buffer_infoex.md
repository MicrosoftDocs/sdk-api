---
UID: NS:wincon._CONSOLE_SCREEN_BUFFER_INFOEX
title: "_CONSOLE_SCREEN_BUFFER_INFOEX"
author: windows-driver-content
description: Contains extended information about a console screen buffer.
old-location: consoles\console_screen_buffer_infoex.htm
old-project: consoles
ms.assetid: 6ed40df3-063d-41c9-8637-510c95104603
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCONSOLE_SCREEN_BUFFER_INFOEX, CONSOLE_SCREEN_BUFFER_INFOEX, CONSOLE_SCREEN_BUFFER_INFOEX structure [Consoles], PCONSOLE_SCREEN_BUFFER_INFOEX, PCONSOLE_SCREEN_BUFFER_INFOEX structure pointer [Consoles], _CONSOLE_SCREEN_BUFFER_INFOEX, base.console_screen_buffer_infoex, consoles.console_screen_buffer_infoex, wincon/CONSOLE_SCREEN_BUFFER_INFOEX, wincon/PCONSOLE_SCREEN_BUFFER_INFOEX"
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
req.typenames: CONSOLE_SCREEN_BUFFER_INFOEX, *PCONSOLE_SCREEN_BUFFER_INFOEX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	CONSOLE_SCREEN_BUFFER_INFOEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CONSOLE_SCREEN_BUFFER_INFOEX structure


## -description


Contains extended information about a console screen buffer.


## -struct-fields




### -field cbSize

The size of this structure, in bytes.


### -field dwSize

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that contains the size of the console screen buffer, in character columns and rows.


### -field dwCursorPosition

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that contains the column and row coordinates of the cursor in the console screen buffer.


### -field wAttributes

The attributes of the characters written to a screen buffer by the 
<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> and 
<a href="https://msdn.microsoft.com/1a13d9ef-75a9-49fd-9717-207f18612b59">WriteConsole</a> functions, or echoed to a screen buffer by the 
<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> and 
<a href="https://msdn.microsoft.com/1aa9ecac-a9b9-4e6d-9206-7a57013de657">ReadConsole</a> functions. For more information, see 
<a href="console_screen_buffers.htm">Character Attributes</a>.


### -field srWindow

A 
<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a> structure that contains the console screen buffer coordinates of the upper-left and lower-right corners of the display window.


### -field dwMaximumWindowSize

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that contains the maximum size of the console window, in character columns and rows, given the current screen buffer size and font and the screen size.


### -field wPopupAttributes

The fill attribute for console pop-ups.


### -field bFullscreenSupported

If this member is TRUE, full-screen mode is supported; otherwise, it is not.


### -field ColorTable

An array of <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> values that describe the console's color settings.


## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/60534226-d26f-44e2-a4cc-64811882e308">GetConsoleScreenBufferInfoEx</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>



<a href="https://msdn.microsoft.com/ff851144-eee9-4410-8fd1-28aa24fc25f1">SetConsoleScreenBufferInfoEx</a>
 

 

