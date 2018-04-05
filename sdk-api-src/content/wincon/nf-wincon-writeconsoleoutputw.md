---
UID: NF:wincon.WriteConsoleOutputW
title: WriteConsoleOutputW function
author: windows-driver-content
description: Writes character and color attribute data to a specified rectangular block of character cells in a console screen buffer.
old-location: consoles\writeconsoleoutput.htm
old-project: consoles
ms.assetid: a98b8118-97ce-4dd4-a337-122d4a76f232
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WriteConsoleOutput, WriteConsoleOutput function [Consoles], WriteConsoleOutputA, WriteConsoleOutputW, _win32_writeconsoleoutput, base.writeconsoleoutput, consoles.writeconsoleoutput, wincon/WriteConsoleOutput, wincon/WriteConsoleOutputA, wincon/WriteConsoleOutputW
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
req.unicode-ansi: WriteConsoleOutputW (Unicode) and WriteConsoleOutputA (ANSI)
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
-	WriteConsoleOutput
-	WriteConsoleOutputA
-	WriteConsoleOutputW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WriteConsoleOutputW function


## -description


Writes character and color attribute data to a specified rectangular block of character cells in a console screen buffer. The data to be written is taken from a correspondingly sized rectangular block at a specified location in the source buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpBuffer [in]

The data to be written to the console screen buffer. This pointer is treated as the origin of a two-dimensional array of 
<a href="https://msdn.microsoft.com/5574a862-b262-41af-8862-e9837c5c7b5f">CHAR_INFO</a> structures whose size is specified by the <i>dwBufferSize</i> parameter.

The storage for this buffer is allocated from a shared heap for the process that is 64 KB in size. The maximum size of the buffer will depend on heap usage.


### -param dwBufferSize [in]

The size of the buffer pointed to by the <i>lpBuffer</i> parameter, in character cells. The <b>X</b> member of the 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure is the number of columns; the <b>Y</b> member is the number of rows.


### -param dwBufferCoord [in]

The coordinates of the upper-left cell in the buffer pointed to by the <i>lpBuffer</i> parameter. The <b>X</b> member of the 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure is the column, and the <b>Y</b> member is the row.


### -param lpWriteRegion [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a> structure. On input, the structure members specify the upper-left and lower-right coordinates of the console screen buffer rectangle to write to. On output, the structure members specify the actual rectangle that was used.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>WriteConsoleOutput</b> treats the source buffer and the destination screen buffer as two-dimensional arrays (columns and rows of character cells). The rectangle pointed to by the <i>lpWriteRegion</i> parameter specifies the size and location of the block to be written to in the console screen buffer. A rectangle of the same size is located with its upper-left cell at the coordinates of the <i>dwBufferCoord</i> parameter in the <i>lpBuffer</i> array. Data from the cells that are in the intersection of this rectangle and the source buffer rectangle (whose dimensions are specified by the <i>dwBufferSize</i> parameter) is written to the destination rectangle.

Cells in the destination rectangle whose corresponding source location are outside the boundaries of the source buffer rectangle are left unaffected by the write operation. In other words, these are the cells for which no data is available to be written.

Before 
<b>WriteConsoleOutput</b> returns, it sets the members of <i>lpWriteRegion</i> to the actual screen buffer rectangle affected by the write operation. This rectangle reflects the cells in the destination rectangle for which there existed a corresponding cell in the source buffer, because 
<b>WriteConsoleOutput</b> clips the dimensions of the destination rectangle to the boundaries of the console screen buffer.

If the rectangle specified by <i>lpWriteRegion</i> lies completely outside the boundaries of the console screen buffer, or if the corresponding rectangle is positioned completely outside the boundaries of the source buffer, no data is written. In this case, the function returns with the members of the structure pointed to by the <i>lpWriteRegion</i> parameter set such that the <b>Right</b> member is less than the <b>Left</b>, or the <b>Bottom</b> member is less than the <b>Top</b>. To determine the size of the console screen buffer, use the 
<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a> function.

<b>WriteConsoleOutput</b> has no effect on the cursor position.

This function uses either Unicode characters or 8-bit characters from the console's current code page. The console's code page defaults initially to the system's OEM code page. To change the console's code page, use the 
<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a> or 
<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a> functions, or use the <b>chcp</b> or <b>mode con cp select=</b> commands.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/eaa57723-f003-4e90-8156-be8c3b42b912">Reading and Writing Blocks of Characters and Attributes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5574a862-b262-41af-8862-e9837c5c7b5f">CHAR_INFO</a>



<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a>



<a href="https://msdn.microsoft.com/94185428-e8c7-4926-93ec-867b8c97b4ca">Low-Level Console Output Functions</a>



<a href="https://msdn.microsoft.com/d1391684-6a8f-4b5e-9706-11970a957710">ReadConsoleOutput</a>



<a href="https://msdn.microsoft.com/c3e35779-a487-47f1-8d07-0d5fae99d54a">ReadConsoleOutputAttribute</a>



<a href="https://msdn.microsoft.com/f47464a9-6c59-4f15-abd0-be29ab515698">ReadConsoleOutputCharacter</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>



<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a>



<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a>



<a href="https://msdn.microsoft.com/52a9d6e5-072e-4411-9945-10bd3dd61e25">WriteConsoleOutputAttribute</a>



<a href="https://msdn.microsoft.com/7cc935ea-6b19-4494-b746-259aa7aaa9cc">WriteConsoleOutputCharacter</a>
 

 

