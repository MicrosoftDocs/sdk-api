---
UID: NF:wincon.FillConsoleOutputAttribute
title: FillConsoleOutputAttribute function
author: windows-driver-content
description: Sets the character attributes for a specified number of character cells, beginning at the specified coordinates in a screen buffer.
old-location: consoles\fillconsoleoutputattribute.htm
old-project: consoles
ms.assetid: 09440263-71c4-4b7a-8fc6-a2b4fcd677ff
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FillConsoleOutputAttribute, FillConsoleOutputAttribute function [Consoles], _win32_fillconsoleoutputattribute, base.fillconsoleoutputattribute, consoles.fillconsoleoutputattribute, wincon/FillConsoleOutputAttribute
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
-	FillConsoleOutputAttribute
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FillConsoleOutputAttribute function


## -description


Sets the character attributes for a specified number of character cells, beginning at the specified coordinates in a screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param wAttribute [in]

The attributes to use when writing to the console screen buffer. For more information, see 
<a href="console_screen_buffers.htm">Character Attributes</a>.


### -param nLength [in]

The number of character cells to be set to the specified color attributes.


### -param dwWriteCoord [in]

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that specifies the character coordinates of the first cell whose attributes are to be set.


### -param lpNumberOfAttrsWritten [out]

A pointer to a variable that receives the number of character cells whose attributes were actually set.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the number of character cells whose attributes are to be set extends beyond the end of the specified row in the console screen buffer, the cells of the next row are set. If the number of cells to write to extends beyond the end of the console screen buffer, the cells are written up to the end of the console screen buffer.

The character values at the positions written to are not changed.




## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/37579cc9-14b3-4fd9-81ed-abaad5c7bd1a">FillConsoleOutputCharacter</a>



<a href="https://msdn.microsoft.com/94185428-e8c7-4926-93ec-867b8c97b4ca">Low-Level Console Output Functions</a>



<a href="https://msdn.microsoft.com/9fba5bb5-b999-4abd-ab39-7a63d58b8074">SetConsoleTextAttribute</a>



<a href="https://msdn.microsoft.com/52a9d6e5-072e-4411-9945-10bd3dd61e25">WriteConsoleOutputAttribute</a>
 

 

