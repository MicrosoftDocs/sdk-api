---
UID: NF:wincon.GetConsoleAliasExesLengthA
title: GetConsoleAliasExesLengthA function
author: windows-driver-content
description: Retrieves the required size for the buffer used by the GetConsoleAliasExes function.
old-location: consoles\getconsolealiasexeslength.htm
old-project: consoles
ms.assetid: 4f23bbb1-3e43-47a9-b91a-e91529b07fb5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleAliasExesLength, GetConsoleAliasExesLength function [Consoles], GetConsoleAliasExesLengthA, GetConsoleAliasExesLengthW, base.getconsolealiasexeslength, consoles.getconsolealiasexeslength, wincon/GetConsoleAliasExesLength, wincon/GetConsoleAliasExesLengthA, wincon/GetConsoleAliasExesLengthW
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
req.unicode-ansi: GetConsoleAliasExesLengthW (Unicode) and GetConsoleAliasExesLengthA (ANSI)
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
-	GetConsoleAliasExesLength
-	GetConsoleAliasExesLengthA
-	GetConsoleAliasExesLengthW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleAliasExesLengthA function


## -description


Retrieves the required size for the buffer used by the <a href="https://msdn.microsoft.com/c229de09-cfa6-4829-9c9a-8ff63500eaf4">GetConsoleAliasExes</a> function.


## -parameters






## -returns



The size of the buffer required to store the names of all executable files that have console aliases defined, in bytes.




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
 

 

