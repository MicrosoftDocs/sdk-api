---
UID: NF:wincon.GetConsoleCursorInfo
title: GetConsoleCursorInfo function
author: windows-driver-content
description: Retrieves information about the size and visibility of the cursor for the specified console screen buffer.
old-location: consoles\getconsolecursorinfo.htm
old-project: consoles
ms.assetid: 6200577d-8d84-46bd-9330-d0b6cbbb3e52
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleCursorInfo, GetConsoleCursorInfo function [Consoles], _win32_getconsolecursorinfo, base.getconsolecursorinfo, consoles.getconsolecursorinfo, wincon/GetConsoleCursorInfo
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
-	GetConsoleCursorInfo
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleCursorInfo function


## -description


Retrieves information about the size and visibility of the cursor for the specified console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpConsoleCursorInfo [out]

A pointer to a 
<a href="https://msdn.microsoft.com/0e71ce8c-e008-4bd7-922e-c44484b425ef">CONSOLE_CURSOR_INFO</a> structure that receives information about the console's cursor.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0e71ce8c-e008-4bd7-922e-c44484b425ef">CONSOLE_CURSOR_INFO</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f94995fc-5f5f-4fcd-969d-7e10020634c2">Console Screen Buffers</a>



<a href="https://msdn.microsoft.com/c98cbffb-18de-41e8-bba7-5fb46a0c5d25">SetConsoleCursorInfo</a>
 

 

