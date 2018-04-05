---
UID: NF:wincon.GetLargestConsoleWindowSize
title: GetLargestConsoleWindowSize function
author: windows-driver-content
description: Retrieves the size of the largest possible console window, based on the current font and the size of the display.
old-location: consoles\getlargestconsolewindowsize.htm
old-project: consoles
ms.assetid: 3e5897f3-4987-4a82-ab19-06c0b231ba67
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetLargestConsoleWindowSize, GetLargestConsoleWindowSize function [Consoles], _win32_getlargestconsolewindowsize, base.getlargestconsolewindowsize, consoles.getlargestconsolewindowsize, wincon/GetLargestConsoleWindowSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
-	API-MS-Win-Core-Console-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
-	GetLargestConsoleWindowSize
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetLargestConsoleWindowSize function


## -description


Retrieves the size of the largest possible console window, based on the current font and the size of the display.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer.


## -returns



If the function succeeds, the return value is a 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that specifies the number of character cell rows (<b>X</b> member) and columns (<b>Y</b> member) in the largest possible console window. Otherwise, the members of the structure are zero.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function does not take into consideration the size of the console screen buffer, which means that the window size returned may be larger than the size of the console screen buffer. The 
<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a> function can be used to determine the maximum size of the console window, given the current screen buffer size, the current font, and the display size.




## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a>



<a href="https://msdn.microsoft.com/ad16a8fe-ca91-41d6-93b1-8cce6d54b1da">SetConsoleWindowInfo</a>



<a href="https://msdn.microsoft.com/55246039-31eb-41ca-ad8e-d314cb508644">Window and Screen Buffer Size</a>
 

 

