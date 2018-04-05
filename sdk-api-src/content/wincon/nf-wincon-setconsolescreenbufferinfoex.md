---
UID: NF:wincon.SetConsoleScreenBufferInfoEx
title: SetConsoleScreenBufferInfoEx function
author: windows-driver-content
description: Sets extended information about the specified console screen buffer.
old-location: consoles\setconsolescreenbufferinfoex.htm
old-project: consoles
ms.assetid: ff851144-eee9-4410-8fd1-28aa24fc25f1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleScreenBufferInfoEx, SetConsoleScreenBufferInfoEx function [Consoles], base.setconsolescreenbufferinfoex, consoles.setconsolescreenbufferinfoex, wincon/SetConsoleScreenBufferInfoEx
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
-	SetConsoleScreenBufferInfoEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleScreenBufferInfoEx function


## -description


Sets extended information about the specified console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpConsoleScreenBufferInfoEx [in]

A <a href="https://msdn.microsoft.com/6ed40df3-063d-41c9-8637-510c95104603">CONSOLE_SCREEN_BUFFER_INFOEX</a> structure that contains the console screen buffer information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/6ed40df3-063d-41c9-8637-510c95104603">CONSOLE_SCREEN_BUFFER_INFOEX</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/60534226-d26f-44e2-a4cc-64811882e308">GetConsoleScreenBufferInfoEx</a>
 

 

