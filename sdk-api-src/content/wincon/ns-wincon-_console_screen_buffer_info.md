---
UID: NS:wincon._CONSOLE_SCREEN_BUFFER_INFO
title: "_CONSOLE_SCREEN_BUFFER_INFO"
author: windows-driver-content
description: Contains information about a console screen buffer.
old-location: consoles\console_screen_buffer_info_str.htm
old-project: consoles
ms.assetid: 586b3e0f-2f6b-4a03-b8e4-602a892be56d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCONSOLE_SCREEN_BUFFER_INFO, CONSOLE_SCREEN_BUFFER_INFO, CONSOLE_SCREEN_BUFFER_INFO structure [Consoles], _CONSOLE_SCREEN_BUFFER_INFO, _win32_console_screen_buffer_info_str, base.console_screen_buffer_info_str, consoles.console_screen_buffer_info_str, wincon/CONSOLE_SCREEN_BUFFER_INFO"
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
req.typenames: CONSOLE_SCREEN_BUFFER_INFO, *PCONSOLE_SCREEN_BUFFER_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	CONSOLE_SCREEN_BUFFER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CONSOLE_SCREEN_BUFFER_INFO structure


## -description


Contains information about a console screen buffer.


## -struct-fields




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


## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a>



<a href="https://msdn.microsoft.com/1aa9ecac-a9b9-4e6d-9206-7a57013de657">ReadConsole</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>



<a href="https://msdn.microsoft.com/1a13d9ef-75a9-49fd-9717-207f18612b59">WriteConsole</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

