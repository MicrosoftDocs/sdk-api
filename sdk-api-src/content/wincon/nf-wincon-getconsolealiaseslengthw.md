---
UID: NF:wincon.GetConsoleAliasesLengthW
title: GetConsoleAliasesLengthW function
author: windows-driver-content
description: Retrieves the required size for the buffer used by the GetConsoleAliases function.
old-location: consoles\getconsolealiaseslength.htm
old-project: consoles
ms.assetid: 29e49eba-0864-4ed7-af82-1ba639261c40
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleAliasesLength, GetConsoleAliasesLength function [Consoles], GetConsoleAliasesLengthA, GetConsoleAliasesLengthW, base.getconsolealiaseslength, consoles.getconsolealiaseslength, wincon/GetConsoleAliasesLength, wincon/GetConsoleAliasesLengthA, wincon/GetConsoleAliasesLengthW
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
req.unicode-ansi: GetConsoleAliasesLengthW (Unicode) and GetConsoleAliasesLengthA (ANSI)
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
-	GetConsoleAliasesLength
-	GetConsoleAliasesLengthA
-	GetConsoleAliasesLengthW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleAliasesLengthW function


## -description


Retrieves the required size for the buffer used by the <a href="https://msdn.microsoft.com/92eefa4e-ffde-4886-afde-5aecf450b425">GetConsoleAliases</a> function.


## -parameters




### -param ExeName

TBD




#### - lpExeName [in]

The name of the executable file whose console aliases are to be retrieved.


## -returns



The size of the buffer required to store all console aliases defined for this executable file, in bytes.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/e4072c3c-cf32-4992-847e-efdb846e5784">AddConsoleAlias</a>



<a href="https://msdn.microsoft.com/8169708b-83da-47ef-94be-eca3ca7d0a5b">Console Aliases</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/e8514f24-8121-4fad-94bb-c9eedf7a700d">GetConsoleAlias</a>



<a href="https://msdn.microsoft.com/c229de09-cfa6-4829-9c9a-8ff63500eaf4">GetConsoleAliasExes</a>



<a href="https://msdn.microsoft.com/92eefa4e-ffde-4886-afde-5aecf450b425">GetConsoleAliases</a>
 

 

