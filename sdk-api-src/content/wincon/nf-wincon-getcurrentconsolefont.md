---
UID: NF:wincon.GetCurrentConsoleFont
title: GetCurrentConsoleFont function
author: windows-driver-content
description: Retrieves information about the current console font.
old-location: consoles\getcurrentconsolefont.htm
old-project: consoles
ms.assetid: 347508ea-5c15-4568-b99f-1e7f5cdac8c1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetCurrentConsoleFont, GetCurrentConsoleFont function [Consoles], _win32_getcurrentconsolefont, base.getcurrentconsolefont, consoles.getcurrentconsolefont, wincon/GetCurrentConsoleFont
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
api_name:
-	GetCurrentConsoleFont
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCurrentConsoleFont function


## -description


Retrieves information about the current console font.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param bMaximumWindow [in]

If this parameter is <b>TRUE</b>, font information is retrieved for the maximum window size. If this parameter is <b>FALSE</b>, font information is retrieved for the current window size.


### -param lpConsoleCurrentFont [out]

A pointer to a 
<a href="https://msdn.microsoft.com/380b8183-1964-46f2-a511-01f39f21f5c5">CONSOLE_FONT_INFO</a> structure that receives the requested font information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/380b8183-1964-46f2-a511-01f39f21f5c5">CONSOLE_FONT_INFO</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f94995fc-5f5f-4fcd-969d-7e10020634c2">Console Screen Buffers</a>



<a href="https://msdn.microsoft.com/51b1f58d-b3fb-4e09-8398-671b3959bb01">GetConsoleFontSize</a>
 

 

