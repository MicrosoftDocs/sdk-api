---
UID: NF:wincon.SetConsoleDisplayMode
title: SetConsoleDisplayMode function
author: windows-driver-content
description: Sets the display mode of the specified console screen buffer.
old-location: consoles\setconsoledisplaymode.htm
old-project: consoles
ms.assetid: 27437a85-f784-41fc-8279-9fe089b0a744
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CONSOLE_FULLSCREEN_MODE, CONSOLE_WINDOWED_MODE, SetConsoleDisplayMode, SetConsoleDisplayMode function [Consoles], base.setconsoledisplaymode, consoles.setconsoledisplaymode, wincon/SetConsoleDisplayMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WICMetadataPattern
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
api_name:
-	SetConsoleDisplayMode
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleDisplayMode function


## -description


Sets the display mode of the specified console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer.


### -param dwFlags [in]

The display mode of the console. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_FULLSCREEN_MODE"></a><a id="console_fullscreen_mode"></a><dl>
<dt><b>CONSOLE_FULLSCREEN_MODE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Text is displayed in full-screen mode.

</td>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_WINDOWED_MODE"></a><a id="console_windowed_mode"></a><dl>
<dt><b>CONSOLE_WINDOWED_MODE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Text is displayed in a console window.

</td>
</tr>
</table>
 


### -param lpNewScreenBufferDimensions [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that receives the new dimensions of the screen buffer, in characters.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f0dcc123-3b12-44c4-8f94-920203f5198e">Console Modes</a>



<a href="https://msdn.microsoft.com/e19ff900-a671-41d3-a9c8-9e4507c47eff">GetConsoleDisplayMode</a>
 

 

