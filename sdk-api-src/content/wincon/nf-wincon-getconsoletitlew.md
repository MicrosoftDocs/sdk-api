---
UID: NF:wincon.GetConsoleTitleW
title: GetConsoleTitleW function
author: windows-driver-content
description: Retrieves the title for the current console window.
old-location: consoles\getconsoletitle.htm
old-project: consoles
ms.assetid: c58bba36-9813-4bdc-83bf-30d55f8d7d79
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleTitle, GetConsoleTitle function [Consoles], GetConsoleTitleA, GetConsoleTitleW, _win32_getconsoletitle, base.getconsoletitle, consoles.getconsoletitle, wincon/GetConsoleTitle, wincon/GetConsoleTitleA, wincon/GetConsoleTitleW
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
req.unicode-ansi: GetConsoleTitleW (Unicode) and GetConsoleTitleA (ANSI)
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
-	API-Ms-Win-Core-Console-Ansi-L2-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	GetConsoleTitle
-	GetConsoleTitleA
-	GetConsoleTitleW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleTitleW function


## -description


Retrieves the title for the current console window.


## -parameters




### -param lpConsoleTitle [out]

A pointer to a buffer that receives a null-terminated string containing the title. If the buffer is too small to store the title, the function stores as many characters of the title as will fit in the buffer, ending with a null terminator.

The storage for this buffer is allocated from a shared heap for the process that is 64 KB in size. The maximum size of the buffer will depend on heap usage.


### -param nSize [in]

The size of the buffer pointed to by the <i>lpConsoleTitle</i> parameter, in characters.


## -returns




						If the function succeeds, the return value is the length of the console window's title, in characters.

If the function fails, the return value is zero and  
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the error code.




## -remarks



To set the title for a console window, use the 
<a href="https://msdn.microsoft.com/f1db449b-0dd0-4d61-bb79-b7da9a5168f4">SetConsoleTitle</a> function. To retrieve the original title string, use the <a href="https://msdn.microsoft.com/e3dd02f4-4899-4df0-a960-3b2625c15fee">GetConsoleOriginalTitle</a> function.

This function uses either Unicode characters or 8-bit characters from the console's current code page. The console's code page defaults initially to the system's OEM code page. To change the console's code page, use the 
<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a> or 
<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a> functions, or use the <b>chcp</b> or <b>mode con cp select=</b> commands.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/f1db449b-0dd0-4d61-bb79-b7da9a5168f4">SetConsoleTitle</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/e3dd02f4-4899-4df0-a960-3b2625c15fee">GetConsoleOriginalTitle</a>



<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a>



<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a>



<a href="https://msdn.microsoft.com/f1db449b-0dd0-4d61-bb79-b7da9a5168f4">SetConsoleTitle</a>
 

 

