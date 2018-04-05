---
UID: NF:wincon.GetConsoleOriginalTitleA
title: GetConsoleOriginalTitleA function
author: windows-driver-content
description: Retrieves the original title for the current console window.
old-location: consoles\getconsoleoriginaltitle.htm
old-project: consoles
ms.assetid: e3dd02f4-4899-4df0-a960-3b2625c15fee
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleOriginalTitle, GetConsoleOriginalTitle function [Consoles], GetConsoleOriginalTitleA, GetConsoleOriginalTitleW, base.getconsoleoriginaltitle, consoles.getconsoleoriginaltitle, wincon/GetConsoleOriginalTitle, wincon/GetConsoleOriginalTitleA, wincon/GetConsoleOriginalTitleW
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
req.unicode-ansi: GetConsoleOriginalTitleW (Unicode) and GetConsoleOriginalTitleA (ANSI)
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
-	GetConsoleOriginalTitle
-	GetConsoleOriginalTitleA
-	GetConsoleOriginalTitleW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleOriginalTitleA function


## -description


Retrieves the original title for the current console window.


## -parameters




### -param lpConsoleTitle [out]

A pointer to a buffer that receives a null-terminated string containing the original title.

The storage for this buffer is allocated from a shared heap for the process that is 64 KB in size. The maximum size of the buffer will depend on heap usage.


### -param nSize [in]

The size of the <i>lpConsoleTitle</i> buffer, in characters.


## -returns




						If the function succeeds, the return value is the length of the string copied to the buffer, in characters.

If the buffer is not large enough to store the title, the return value is zero and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_SUCCESS</b>.

If the function fails, the return value is zero and  
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the error code.




## -remarks



To set the title for a console window, use the 
<a href="https://msdn.microsoft.com/f1db449b-0dd0-4d61-bb79-b7da9a5168f4">SetConsoleTitle</a> function. To retrieve the current title string, use the <a href="https://msdn.microsoft.com/c58bba36-9813-4bdc-83bf-30d55f8d7d79">GetConsoleTitle</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/c58bba36-9813-4bdc-83bf-30d55f8d7d79">GetConsoleTitle</a>



<a href="https://msdn.microsoft.com/f1db449b-0dd0-4d61-bb79-b7da9a5168f4">SetConsoleTitle</a>
 

 

