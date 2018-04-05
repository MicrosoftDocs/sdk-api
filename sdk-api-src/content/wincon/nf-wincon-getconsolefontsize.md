---
UID: NF:wincon.GetConsoleFontSize
title: GetConsoleFontSize function
author: windows-driver-content
description: Retrieves the size of the font used by the specified console screen buffer.
old-location: consoles\getconsolefontsize.htm
old-project: consoles
ms.assetid: 51b1f58d-b3fb-4e09-8398-671b3959bb01
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleFontSize, GetConsoleFontSize function [Consoles], _win32_getconsolefontsize, base.getconsolefontsize, consoles.getconsolefontsize, wincon/GetConsoleFontSize
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
-	GetConsoleFontSize
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleFontSize function


## -description


Retrieves the size of the font used by the specified console screen buffer.


## -parameters




### -param hConsoleOutput [in]

A handle to the console screen buffer. The handle must have the <b>GENERIC_READ</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param nFont [in]

The index of the font whose size is to be retrieved. This index is obtained by calling the 
<a href="https://msdn.microsoft.com/347508ea-5c15-4568-b99f-1e7f5cdac8c1">GetCurrentConsoleFont</a> function.


## -returns



If the function succeeds, the return value is a 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that contains the width and height of each character in the font, in logical units. The <b>X</b> member contains the width, while the <b>Y</b> member contains the height.

If the function fails, the width and the height are zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f94995fc-5f5f-4fcd-969d-7e10020634c2">Console Screen Buffers</a>



<a href="https://msdn.microsoft.com/347508ea-5c15-4568-b99f-1e7f5cdac8c1">GetCurrentConsoleFont</a>
 

 

