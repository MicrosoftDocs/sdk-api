---
UID: NF:wincon.WriteConsoleInputW
title: WriteConsoleInputW function
author: windows-driver-content
description: Writes data directly to the console input buffer.
old-location: consoles\writeconsoleinput.htm
old-project: consoles
ms.assetid: ad06231f-5063-4aff-b14d-8df5e6e42430
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WriteConsoleInput, WriteConsoleInput function [Consoles], WriteConsoleInputA, WriteConsoleInputW, _win32_writeconsoleinput, base.writeconsoleinput, consoles.writeconsoleinput, wincon/WriteConsoleInput, wincon/WriteConsoleInputA, wincon/WriteConsoleInputW
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
req.unicode-ansi: WriteConsoleInputW (Unicode) and WriteConsoleInputA (ANSI)
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
-	WriteConsoleInput
-	WriteConsoleInputA
-	WriteConsoleInputW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WriteConsoleInputW function


## -description


Writes data directly to the console input buffer.


## -parameters




### -param hConsoleInput [in]

A handle to the console input buffer. The handle must have the <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param lpBuffer [in]

A pointer to an array of 
<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a> structures that contain data to be written to the input buffer.

The storage for this buffer is allocated from a shared heap for the process that is 64 KB in size. The maximum size of the buffer will depend on heap usage.


### -param nLength [in]

The number of input records to be written.


### -param lpNumberOfEventsWritten [out]

A pointer to a variable that receives the number of input records actually written.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>WriteConsoleInput</b> places input records into the input buffer behind any pending events in the buffer. The input buffer grows dynamically, if necessary, to hold as many events as are written.

This function uses either Unicode characters or 8-bit characters from the console's current code page. The console's code page defaults initially to the system's OEM code page. To change the console's code page, use the 
<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a> or 
<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a> functions, or use the <b>chcp</b> or <b>mode con cp select=</b> commands.  




## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a>



<a href="https://msdn.microsoft.com/41488614-ca7c-4207-b706-f7776423c7ba">Low-Level Console Input Functions</a>



<a href="https://msdn.microsoft.com/d287c66d-def1-4794-a95b-fa7c93e7bd35">MapVirtualKey</a>



<a href="https://msdn.microsoft.com/9982dc20-43bd-4ee3-a68d-157c9134daca">PeekConsoleInput</a>



<a href="https://msdn.microsoft.com/5a9f7b18-cdea-4041-a377-5532d30e0105">ReadConsoleInput</a>



<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a>



<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a>



<a href="https://msdn.microsoft.com/ad94ff40-131a-4632-97f6-0e80e28a215f">VkKeyScan</a>
 

 

