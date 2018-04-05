---
UID: NF:wincon.GetConsoleScreenBufferInfo
title: GetConsoleScreenBufferInfo function
author: windows-driver-content
description: Retrieves information about the specified console screen buffer.
old-location: consoles\getconsolescreenbufferinfo.htm
old-project: consoles
ms.assetid: eafe819e-a99a-4ce1-8898-8860444a31af
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleScreenBufferInfo, GetConsoleScreenBufferInfo function [Consoles], _win32_getconsolescreenbufferinfo, base.getconsolescreenbufferinfo, consoles.getconsolescreenbufferinfo, wincon/GetConsoleScreenBufferInfo
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
-	GetConsoleScreenBufferInfo
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleScreenBufferInfo function


## -description


Retrieves information about the specified console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpConsoleScreenBufferInfo [out]

A pointer to a 
<a href="https://msdn.microsoft.com/586b3e0f-2f6b-4a03-b8e4-602a892be56d">CONSOLE_SCREEN_BUFFER_INFO</a> structure that receives the console screen buffer information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The rectangle returned in the <b>srWindow</b> member of the 
<a href="https://msdn.microsoft.com/586b3e0f-2f6b-4a03-b8e4-602a892be56d">CONSOLE_SCREEN_BUFFER_INFO</a> structure can be modified and then passed to the 
<a href="https://msdn.microsoft.com/ad16a8fe-ca91-41d6-93b1-8cce6d54b1da">SetConsoleWindowInfo</a> function to scroll the console screen buffer in the window, to change the size of the window, or both.

All coordinates returned in the 
<a href="https://msdn.microsoft.com/586b3e0f-2f6b-4a03-b8e4-602a892be56d">CONSOLE_SCREEN_BUFFER_INFO</a> structure are in character-cell coordinates, where the origin (0, 0) is at the upper-left corner of the console screen buffer.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/bc300349-9bfa-4417-92ad-57a05a658ce5">Scrolling a Screen Buffer's Window</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/586b3e0f-2f6b-4a03-b8e4-602a892be56d">CONSOLE_SCREEN_BUFFER_INFO</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/3e5897f3-4987-4a82-ab19-06c0b231ba67">GetLargestConsoleWindowSize</a>



<a href="https://msdn.microsoft.com/8e9abada-a64e-429f-8286-ced1169c7104">SetConsoleCursorPosition</a>



<a href="https://msdn.microsoft.com/50bf1973-5604-42fe-bbeb-611ddc240bdd">SetConsoleScreenBufferSize</a>



<a href="https://msdn.microsoft.com/ad16a8fe-ca91-41d6-93b1-8cce6d54b1da">SetConsoleWindowInfo</a>



<a href="https://msdn.microsoft.com/55246039-31eb-41ca-ad8e-d314cb508644">Window and Screen Buffer Size</a>
 

 

