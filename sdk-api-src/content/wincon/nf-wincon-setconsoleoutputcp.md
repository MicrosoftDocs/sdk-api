---
UID: NF:wincon.SetConsoleOutputCP
title: SetConsoleOutputCP function
author: windows-driver-content
description: Sets the output code page used by the console associated with the calling process.
old-location: consoles\setconsoleoutputcp.htm
old-project: consoles
ms.assetid: 0b41e66b-ca19-4d69-9f39-92da158344ef
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleOutputCP, SetConsoleOutputCP function [Consoles], _win32_setconsoleoutputcp, base.setconsoleoutputcp, consoles.setconsoleoutputcp, wincon/SetConsoleOutputCP
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
-	SetConsoleOutputCP
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleOutputCP function


## -description


Sets the output code page used by the console associated with the calling process. A console uses its output code page to translate the character values written by the various output functions into the images displayed in the console window.


## -parameters




### -param wCodePageID [in]

The identifier of the code page to set. For more information, see Remarks.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A code page maps 256 character codes to individual characters. Different code pages include different special characters, typically customized for a language or a group of languages.  

If the current font is a fixed-pitch Unicode font, 
<b>SetConsoleOutputCP</b> changes the mapping of the character values into the glyph set of the font, rather than loading a separate font each time it is called. This affects how extended characters (ASCII value greater than 127) are displayed in a console window. However, if the current font is a raster font, 
<b>SetConsoleOutputCP</b> does not affect how extended characters are displayed.

To find the code pages that are installed  or supported by the operating system, use the <a href="http://go.microsoft.com/fwlink/p/?linkid=178051">EnumSystemCodePages</a> function. The identifiers of the code pages available on the local computer are also stored in the registry under the following key: 


<b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\CodePage</b></p>However, it is better to use <a href="http://go.microsoft.com/fwlink/p/?linkid=178051">EnumSystemCodePages</a>  to enumerate code pages because the registry can differ in different versions of Windows.

To determine whether a particular code page is valid, use the <a href="http://go.microsoft.com/fwlink/p/?linkid=178053">IsValidCodePage</a> function. To retrieve more information about a code page, including its name, use the <a href="https://msdn.microsoft.com/c21ed6fe-85b6-438a-8f53-e30833e0c88a">GetCPInfoEx</a> function. For a list of available code page identifiers, see <a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a>. 

To determine a console's current output code page, use the 
<a href="https://msdn.microsoft.com/c23706c7-ce17-4825-a494-20ca44534d45">GetConsoleOutputCP</a> function. To set and retrieve a console's input code page, use the 
<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a> and 
<a href="https://msdn.microsoft.com/9e0af6d9-0f5c-45b3-a686-22449d26de47">GetConsoleCP</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/98d56bb1-83d2-40aa-adac-fc2e8beab337">Console Code Pages</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/9e0af6d9-0f5c-45b3-a686-22449d26de47">GetConsoleCP</a>



<a href="https://msdn.microsoft.com/c23706c7-ce17-4825-a494-20ca44534d45">GetConsoleOutputCP</a>



<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a>
 

 

