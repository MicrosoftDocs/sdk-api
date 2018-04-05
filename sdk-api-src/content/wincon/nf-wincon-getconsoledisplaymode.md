---
UID: NF:wincon.GetConsoleDisplayMode
title: GetConsoleDisplayMode function
author: windows-driver-content
description: Retrieves the display mode of the current console.
old-location: consoles\getconsoledisplaymode.htm
old-project: consoles
ms.assetid: e19ff900-a671-41d3-a9c8-9e4507c47eff
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CONSOLE_FULLSCREEN, CONSOLE_FULLSCREEN_HARDWARE, GetConsoleDisplayMode, GetConsoleDisplayMode function [Consoles], _win32_getconsoledisplaymode, base.getconsoledisplaymode, consoles.getconsoledisplaymode, wincon/GetConsoleDisplayMode
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
-	GetConsoleDisplayMode
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleDisplayMode function


## -description


Retrieves the display mode of the current console.


## -parameters




### -param lpModeFlags [out]

The display mode of the console. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_FULLSCREEN"></a><a id="console_fullscreen"></a><dl>
<dt><b>CONSOLE_FULLSCREEN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Full-screen console. The console is in this mode as soon as the window is maximized. At this point, the transition to full-screen mode can still fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CONSOLE_FULLSCREEN_HARDWARE"></a><a id="console_fullscreen_hardware"></a><dl>
<dt><b>CONSOLE_FULLSCREEN_HARDWARE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Full-screen console communicating directly with the video hardware. This mode is set after the console is in <b>CONSOLE_FULLSCREEN</b> mode to indicate that the transition to full-screen mode has completed.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f0dcc123-3b12-44c4-8f94-920203f5198e">Console Modes</a>



<a href="https://msdn.microsoft.com/27437a85-f784-41fc-8279-9fe089b0a744">SetConsoleDisplayMode</a>
 

 

