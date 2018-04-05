---
UID: NF:wincon.GetConsoleAliasA
title: GetConsoleAliasA function
author: windows-driver-content
description: Retrieves the text for the specified console alias and executable.
old-location: consoles\getconsolealias.htm
old-project: consoles
ms.assetid: e8514f24-8121-4fad-94bb-c9eedf7a700d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleAlias, GetConsoleAlias function [Consoles], GetConsoleAliasA, GetConsoleAliasW, base.getconsolealias, consoles.getconsolealias, wincon/GetConsoleAlias, wincon/GetConsoleAliasA, wincon/GetConsoleAliasW
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
req.unicode-ansi: GetConsoleAliasW (Unicode) and GetConsoleAliasA (ANSI)
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
-	GetConsoleAlias
-	GetConsoleAliasA
-	GetConsoleAliasW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleAliasA function


## -description


Retrieves the text for the specified console alias and executable.


## -parameters




### -param Source

TBD


### -param TargetBuffer

TBD


### -param TargetBufferLength [in]

The size of the buffer pointed to by <i>lpTargetBuffer</i>, in bytes.


### -param ExeName

TBD




#### - lpExeName [in]

The name of the executable file.


#### - lpSource [in]

The console alias whose text is to be retrieved.


#### - lpTargetBuffer [out]

A pointer to a buffer that receives the text associated with the console alias.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/e4072c3c-cf32-4992-847e-efdb846e5784">AddConsoleAlias</a>



<a href="https://msdn.microsoft.com/8169708b-83da-47ef-94be-eca3ca7d0a5b">Console Aliases</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/c229de09-cfa6-4829-9c9a-8ff63500eaf4">GetConsoleAliasExes</a>



<a href="https://msdn.microsoft.com/92eefa4e-ffde-4886-afde-5aecf450b425">GetConsoleAliases</a>
 

 

