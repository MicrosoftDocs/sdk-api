---
UID: NF:wincon.SetConsoleActiveScreenBuffer
title: SetConsoleActiveScreenBuffer function
author: windows-driver-content
description: Sets the specified screen buffer to be the currently displayed console screen buffer.
old-location: consoles\setconsoleactivescreenbuffer.htm
old-project: consoles
ms.assetid: c026cb94-c8ec-44ee-b432-3870ae3006c2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleActiveScreenBuffer, SetConsoleActiveScreenBuffer function [Consoles], _win32_setconsoleactivescreenbuffer, base.setconsoleactivescreenbuffer, consoles.setconsoleactivescreenbuffer, wincon/SetConsoleActiveScreenBuffer
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
-	SetConsoleActiveScreenBuffer
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleActiveScreenBuffer function


## -description


Sets the specified screen buffer to be the currently displayed console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A console can have multiple screen buffers. 
<b>SetConsoleActiveScreenBuffer</b> determines which one is displayed. You can write to an inactive screen buffer and then use 
<b>SetConsoleActiveScreenBuffer</b> to display the buffer's contents.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/eaa57723-f003-4e90-8156-be8c3b42b912">Reading and Writing Blocks of Characters and Attributes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f94995fc-5f5f-4fcd-969d-7e10020634c2">Console Screen Buffers</a>



<a href="https://msdn.microsoft.com/98bb74e4-dad2-4615-9263-48ba778a06ff">CreateConsoleScreenBuffer</a>
 

 

