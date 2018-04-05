---
UID: NF:wincon.ReadConsoleOutputAttribute
title: ReadConsoleOutputAttribute function
author: windows-driver-content
description: Copies a specified number of character attributes from consecutive cells of a console screen buffer, beginning at a specified location.
old-location: consoles\readconsoleoutputattribute.htm
old-project: consoles
ms.assetid: c3e35779-a487-47f1-8d07-0d5fae99d54a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ReadConsoleOutputAttribute, ReadConsoleOutputAttribute function [Consoles], _win32_readconsoleoutputattribute, base.readconsoleoutputattribute, consoles.readconsoleoutputattribute, wincon/ReadConsoleOutputAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
-	ReadConsoleOutputAttribute
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ReadConsoleOutputAttribute function


## -description


Copies a specified number of character attributes from consecutive cells of a console screen buffer, beginning at a specified location.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpAttribute [out]

A pointer to a buffer that receives the attributes being used by the console screen buffer.

The storage for this buffer is allocated from a shared heap for the process that is 64 KB in size. The maximum size of the buffer will depend on heap usage.

For more information, see 
<a href="console_screen_buffers.htm">Character Attributes</a>.


### -param nLength [in]

The number of screen buffer character cells from which to read. The size of the buffer pointed to by the <i>lpAttribute</i> parameter should be <code>nLength * sizeof(WORD)</code>.


### -param dwReadCoord [in]

The coordinates of the first cell in the console screen buffer from which to read, in characters. The <b>X</b> member of the 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure is the column, and the <b>Y</b> member is the row.


### -param lpNumberOfAttrsRead [out]

A pointer to a variable that receives the number of attributes actually read.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the number of attributes to be read from extends beyond the end of the specified screen buffer row, attributes are read from the next row. If the number of attributes to be read from extends beyond the end of the console screen buffer, attributes up to the end of the console screen buffer are read.




## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/94185428-e8c7-4926-93ec-867b8c97b4ca">Low-Level Console Output Functions</a>



<a href="https://msdn.microsoft.com/d1391684-6a8f-4b5e-9706-11970a957710">ReadConsoleOutput</a>



<a href="https://msdn.microsoft.com/f47464a9-6c59-4f15-abd0-be29ab515698">ReadConsoleOutputCharacter</a>



<a href="https://msdn.microsoft.com/a98b8118-97ce-4dd4-a337-122d4a76f232">WriteConsoleOutput</a>



<a href="https://msdn.microsoft.com/52a9d6e5-072e-4411-9945-10bd3dd61e25">WriteConsoleOutputAttribute</a>



<a href="https://msdn.microsoft.com/7cc935ea-6b19-4494-b746-259aa7aaa9cc">WriteConsoleOutputCharacter</a>
 

 

