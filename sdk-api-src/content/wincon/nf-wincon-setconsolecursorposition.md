---
UID: NF:wincon.SetConsoleCursorPosition
title: SetConsoleCursorPosition function
author: windows-driver-content
description: Sets the cursor position in the specified console screen buffer.
old-location: consoles\setconsolecursorposition.htm
old-project: consoles
ms.assetid: 8e9abada-a64e-429f-8286-ced1169c7104
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleCursorPosition, SetConsoleCursorPosition function [Consoles], _win32_setconsolecursorposition, base.setconsolecursorposition, consoles.setconsolecursorposition, wincon/SetConsoleCursorPosition
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
-	SetConsoleCursorPosition
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleCursorPosition function


## -description


Sets the cursor position in the specified console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param dwCursorPosition [in]

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that specifies the new cursor position, in characters. The coordinates are the column and row of a screen buffer character cell. The coordinates must be within the boundaries of the console screen buffer.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The cursor position determines where characters written by the <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> or 
<a href="https://msdn.microsoft.com/1a13d9ef-75a9-49fd-9717-207f18612b59">WriteConsole</a> function, or echoed by the <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> or 
<a href="https://msdn.microsoft.com/1aa9ecac-a9b9-4e6d-9206-7a57013de657">ReadConsole</a> function, are displayed. To determine the current position of the cursor, use the 
<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a> function.

If the new cursor position is not within the boundaries of the console screen buffer's window, the window origin changes to make the cursor visible.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/0226cd94-86d0-452b-80e6-e0fed8af0a62">Using the High-Level Input and Output Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f94995fc-5f5f-4fcd-969d-7e10020634c2">Console Screen Buffers</a>



<a href="https://msdn.microsoft.com/6200577d-8d84-46bd-9330-d0b6cbbb3e52">GetConsoleCursorInfo</a>



<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a>



<a href="https://msdn.microsoft.com/1aa9ecac-a9b9-4e6d-9206-7a57013de657">ReadConsole</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>



<a href="https://msdn.microsoft.com/c98cbffb-18de-41e8-bba7-5fb46a0c5d25">SetConsoleCursorInfo</a>



<a href="https://msdn.microsoft.com/1a13d9ef-75a9-49fd-9717-207f18612b59">WriteConsole</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

