---
UID: NF:wincon.GetCurrentConsoleFontEx
title: GetCurrentConsoleFontEx function
author: windows-driver-content
description: Retrieves extended information about the current console font.
old-location: consoles\getcurrentconsolefontex.htm
old-project: consoles
ms.assetid: 97d8e730-4110-4be5-b099-0acc1b6f8eb5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetCurrentConsoleFontEx, GetCurrentConsoleFontEx function [Consoles], base.getcurrentconsolefontex, consoles.getcurrentconsolefontex, wincon/GetCurrentConsoleFontEx
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
api_name:
-	GetCurrentConsoleFontEx
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCurrentConsoleFontEx function


## -description


Retrieves extended information about the current console font.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param bMaximumWindow [in]

If this parameter is <b>TRUE</b>, font information is retrieved for the maximum window size. If this parameter is <b>FALSE</b>, font information is retrieved for the current window size.


### -param lpConsoleCurrentFontEx [out]

A pointer to a 
<a href="https://msdn.microsoft.com/e9a087e1-264d-4d48-8adb-771a0e35b511">CONSOLE_FONT_INFOEX</a> structure that receives the requested font information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/e9a087e1-264d-4d48-8adb-771a0e35b511">CONSOLE_FONT_INFOEX</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>
 

 

