---
UID: NF:wincon.SetConsoleScreenBufferSize
title: SetConsoleScreenBufferSize function
author: windows-driver-content
description: Changes the size of the specified console screen buffer.
old-location: consoles\setconsolescreenbuffersize.htm
old-project: consoles
ms.assetid: 50bf1973-5604-42fe-bbeb-611ddc240bdd
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleScreenBufferSize, SetConsoleScreenBufferSize function [Consoles], _win32_setconsolescreenbuffersize, base.setconsolescreenbuffersize, consoles.setconsolescreenbuffersize, wincon/SetConsoleScreenBufferSize
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
-	SetConsoleScreenBufferSize
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleScreenBufferSize function


## -description


Changes the size of the specified console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param dwSize [in]

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that specifies the new size of the console screen buffer, in character rows and columns. The specified width and height cannot be less than the width and height of the console screen buffer's window. The specified dimensions also cannot be less than the minimum size allowed by the system. This minimum depends on the current font size for the console (selected by the user) and the <b>SM_CXMIN</b> and <b>SM_CYMIN</b> values returned by the 
<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/6e536658-8a27-478e-82ee-d1e11f351301">Console Input Buffer</a>



<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a>



<a href="https://msdn.microsoft.com/ad16a8fe-ca91-41d6-93b1-8cce6d54b1da">SetConsoleWindowInfo</a>
 

 

