---
UID: NF:wincon.PeekConsoleInputW
title: PeekConsoleInputW function
author: windows-driver-content
description: Reads data from the specified console input buffer without removing it from the buffer.
old-location: consoles\peekconsoleinput.htm
old-project: consoles
ms.assetid: 9982dc20-43bd-4ee3-a68d-157c9134daca
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PeekConsoleInput, PeekConsoleInput function [Consoles], PeekConsoleInputA, PeekConsoleInputW, _win32_peekconsoleinput, base.peekconsoleinput, consoles.peekconsoleinput, wincon/PeekConsoleInput, wincon/PeekConsoleInputA, wincon/PeekConsoleInputW
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
req.unicode-ansi: PeekConsoleInputW (Unicode) and PeekConsoleInputA (ANSI)
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
-	API-MS-Win-Core-Console-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-Console-l2-1-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	PeekConsoleInput
-	PeekConsoleInputA
-	PeekConsoleInputW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PeekConsoleInputW function


## -description


Reads data from the specified console input buffer without removing it from the buffer.


## -parameters




### -param hConsoleInput [in]

A handle to the console input buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpBuffer [out]

A pointer to an array of 
<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a> structures that receives the input buffer data.

The storage for this buffer is allocated from a shared heap for the process that is 64 KB in size. The maximum size of the buffer will depend on heap usage.


### -param nLength [in]

The size of the array pointed to by the <i>lpBuffer</i> parameter, in array elements.


### -param lpNumberOfEventsRead [out]

A pointer to a variable that receives the number of input records read.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the number of records requested exceeds the number of records available in the buffer, the number available is read. If no data is available, the function returns immediately.

This function uses either Unicode characters or 8-bit characters from the console's current code page. The console's code page defaults initially to the system's OEM code page. To change the console's code page, use the 
<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a> or 
<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a> functions, or use the <b>chcp</b> or <b>mode con cp select=</b> commands.




## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a>



<a href="https://msdn.microsoft.com/5a9f7b18-cdea-4041-a377-5532d30e0105">ReadConsoleInput</a>



<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a>



<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a>



<a href="https://msdn.microsoft.com/ad06231f-5063-4aff-b14d-8df5e6e42430">WriteConsoleInput</a>
 

 

