---
UID: NF:wincon.GetConsoleScreenBufferInfoEx
title: GetConsoleScreenBufferInfoEx function
author: windows-driver-content
description: Retrieves extended information about the specified console screen buffer.
old-location: consoles\getconsolescreenbufferinfoex.htm
old-project: consoles
ms.assetid: 60534226-d26f-44e2-a4cc-64811882e308
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleScreenBufferInfoEx, GetConsoleScreenBufferInfoEx function [Consoles], base.getconsolescreenbufferinfoex, consoles.getconsolescreenbufferinfoex, wincon/GetConsoleScreenBufferInfoEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
-	GetConsoleScreenBufferInfoEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleScreenBufferInfoEx function


## -description


Retrieves extended information about the specified console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpConsoleScreenBufferInfoEx [out]

A <a href="https://msdn.microsoft.com/6ed40df3-063d-41c9-8637-510c95104603">CONSOLE_SCREEN_BUFFER_INFOEX</a> structure that receives the requested console screen buffer information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The rectangle returned in the <b>srWindow</b> member of the 
<a href="https://msdn.microsoft.com/6ed40df3-063d-41c9-8637-510c95104603">CONSOLE_SCREEN_BUFFER_INFOEX</a> structure can be modified and then passed to the 
<a href="https://msdn.microsoft.com/ad16a8fe-ca91-41d6-93b1-8cce6d54b1da">SetConsoleWindowInfo</a> function to scroll the console screen buffer in the window, to change the size of the window, or both.

All coordinates returned in the 
<a href="https://msdn.microsoft.com/6ed40df3-063d-41c9-8637-510c95104603">CONSOLE_SCREEN_BUFFER_INFOEX</a> structure are in character-cell coordinates, where the origin (0, 0) is at the upper-left corner of the console screen buffer.




## -see-also




<a href="https://msdn.microsoft.com/6ed40df3-063d-41c9-8637-510c95104603">CONSOLE_SCREEN_BUFFER_INFOEX</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/ff851144-eee9-4410-8fd1-28aa24fc25f1">SetConsoleScreenBufferInfoEx</a>
 

 

