---
UID: NF:wincon.FlushConsoleInputBuffer
title: FlushConsoleInputBuffer function
author: windows-driver-content
description: Flushes the console input buffer. All input records currently in the input buffer are discarded.
old-location: consoles\flushconsoleinputbuffer.htm
old-project: consoles
ms.assetid: 6f7832d6-1fb2-4ca8-bd07-43123c990851
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FlushConsoleInputBuffer, FlushConsoleInputBuffer function [Consoles], _win32_flushconsoleinputbuffer, base.flushconsoleinputbuffer, consoles.flushconsoleinputbuffer, wincon/FlushConsoleInputBuffer
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
-	FlushConsoleInputBuffer
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FlushConsoleInputBuffer function


## -description


Flushes the console input buffer. All input records currently in the input buffer are discarded.


## -parameters




### -param hConsoleInput [in]

A handle to the console input buffer. The handle must have the <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/1083b4f1-8fa6-4054-a516-3b447c3b0130">GetNumberOfConsoleInputEvents</a>



<a href="https://msdn.microsoft.com/41488614-ca7c-4207-b706-f7776423c7ba">Low-Level Console Input Functions</a>



<a href="https://msdn.microsoft.com/9982dc20-43bd-4ee3-a68d-157c9134daca">PeekConsoleInput</a>



<a href="https://msdn.microsoft.com/5a9f7b18-cdea-4041-a377-5532d30e0105">ReadConsoleInput</a>



<a href="https://msdn.microsoft.com/ad06231f-5063-4aff-b14d-8df5e6e42430">WriteConsoleInput</a>
 

 

