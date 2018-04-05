---
UID: NF:wincon.ReadConsoleOutputA
title: ReadConsoleOutputA function
author: windows-driver-content
description: Reads character and color attribute data from a rectangular block of character cells in a console screen buffer, and the function writes the data to a rectangular block at a specified location in the destination buffer.
old-location: consoles\readconsoleoutput.htm
old-project: consoles
ms.assetid: d1391684-6a8f-4b5e-9706-11970a957710
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ReadConsoleOutput, ReadConsoleOutput function [Consoles], ReadConsoleOutputA, ReadConsoleOutputW, _win32_readconsoleoutput, base.readconsoleoutput, consoles.readconsoleoutput, wincon/ReadConsoleOutput, wincon/ReadConsoleOutputA, wincon/ReadConsoleOutputW
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
req.unicode-ansi: ReadConsoleOutputW (Unicode) and ReadConsoleOutputA (ANSI)
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
-	ReadConsoleOutput
-	ReadConsoleOutputA
-	ReadConsoleOutputW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ReadConsoleOutputA function


## -description


Reads character and color attribute data from a rectangular block of character cells in a console screen buffer, and the function writes the data to a rectangular block at a specified location in the destination buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpBuffer [out]

A pointer to a destination buffer that receives the data read from the console screen buffer. This pointer is treated as the origin of a two-dimensional array of 
<a href="https://msdn.microsoft.com/5574a862-b262-41af-8862-e9837c5c7b5f">CHAR_INFO</a> structures whose size is specified by the <i>dwBufferSize</i> parameter.

The storage for this buffer is allocated from a shared heap for the process that is 64 KB in size. The maximum size of the buffer will depend on heap usage.


### -param dwBufferSize [in]

The size of the <i>lpBuffer</i> parameter, in character cells. The <b>X</b> member of the 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure is the number of columns; the <b>Y</b> member is the number of rows.


### -param dwBufferCoord [in]

The coordinates of the upper-left cell in the <i>lpBuffer</i> parameter that receives the data read from the console screen buffer. The <b>X</b> member of the 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure is the column, and the <b>Y</b> member is the row.


### -param lpReadRegion [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a> structure. On input, the structure members specify the upper-left and lower-right coordinates of the console screen buffer rectangle from which the function is to read. On output, the structure members specify the actual rectangle that was used.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>ReadConsoleOutput</b> treats the console screen buffer and the destination buffer as two-dimensional arrays (columns and rows of character cells). The rectangle pointed to by the <i>lpReadRegion</i> parameter specifies the size and location of the block to be read from the console screen buffer. A destination rectangle of the same size is located with its upper-left cell at the coordinates of the <i>dwBufferCoord</i> parameter in the <i>lpBuffer</i> array. Data read from the cells in the console screen buffer source rectangle is copied to the corresponding cells in the destination buffer. If the corresponding cell is outside the boundaries of the destination buffer rectangle (whose dimensions are specified by the <i>dwBufferSize</i> parameter), the data is not copied.

Cells in the destination buffer corresponding to coordinates that are not within the boundaries of the console screen buffer are left unchanged. In other words, these are the cells for which no screen buffer data is available to be read.

Before 
<b>ReadConsoleOutput</b> returns, it sets the members of the structure pointed to by the <i>lpReadRegion</i> parameter to the actual screen buffer rectangle whose cells were copied into the destination buffer. This rectangle reflects the cells in the source rectangle for which there existed a corresponding cell in the destination buffer, because 
<b>ReadConsoleOutput</b> clips the dimensions of the source rectangle to fit the boundaries of the console screen buffer.

If the rectangle specified by <i>lpReadRegion</i> lies completely outside the boundaries of the console screen buffer, or if the corresponding rectangle is positioned completely outside the boundaries of the destination buffer, no data is copied. In this case, the function returns with the members of the structure pointed to by the <i>lpReadRegion</i> parameter set such that the <b>Right</b> member is less than the <b>Left</b>, or the <b>Bottom</b> member is less than the <b>Top</b>. To determine the size of the console screen buffer, use the 
<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a> function.

The 
<b>ReadConsoleOutput</b> function has no effect on the console screen buffer's cursor position. The contents of the console screen buffer are not changed by the function.

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



<a href="https://msdn.microsoft.com/94185428-e8c7-4926-93ec-867b8c97b4ca">Low-Level Console Output Functions</a>



<a href="https://msdn.microsoft.com/c3e35779-a487-47f1-8d07-0d5fae99d54a">ReadConsoleOutputAttribute</a>



<a href="https://msdn.microsoft.com/f47464a9-6c59-4f15-abd0-be29ab515698">ReadConsoleOutputCharacter</a>



<a href="https://msdn.microsoft.com/62639815-c7e9-4ae2-b152-61290f78422b">SMALL_RECT</a>



<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a>



<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a>



<a href="https://msdn.microsoft.com/a98b8118-97ce-4dd4-a337-122d4a76f232">WriteConsoleOutput</a>
 

 

