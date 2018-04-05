---
UID: NF:wincon.GetConsoleAliasesW
title: GetConsoleAliasesW function
author: windows-driver-content
description: Retrieves all defined console aliases for the specified executable.
old-location: consoles\getconsolealiases.htm
old-project: consoles
ms.assetid: 92eefa4e-ffde-4886-afde-5aecf450b425
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleAliases, GetConsoleAliases function [Consoles], GetConsoleAliasesA, GetConsoleAliasesW, base.getconsolealiases, consoles.getconsolealiases, wincon/GetConsoleAliases, wincon/GetConsoleAliasesA, wincon/GetConsoleAliasesW
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
req.unicode-ansi: GetConsoleAliasesW (Unicode) and GetConsoleAliasesA (ANSI)
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
-	GetConsoleAliases
-	GetConsoleAliasesA
-	GetConsoleAliasesW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleAliasesW function


## -description


Retrieves all defined console aliases for the specified executable.


## -parameters




### -param AliasBuffer

TBD


### -param AliasBufferLength [in]

The size of the buffer pointed to by <i>lpAliasBuffer</i>, in bytes.


### -param ExeName

TBD




#### - lpAliasBuffer [out]

A pointer to a buffer that receives the aliases. 

The format of the data is as follows: <i>Source1</i>=<i>Target1</i>\0<i>Source2</i>=<i>Target2</i>\0... <i>SourceN</i>=<i>TargetN</i>\0, where <i>N</i> is the number of console aliases defined.


#### - lpExeName [in]

The executable file whose aliases are to be retrieved.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To determine the required size  for the <i>lpExeName</i> buffer, use the <a href="https://msdn.microsoft.com/29e49eba-0864-4ed7-af82-1ba639261c40">GetConsoleAliasesLength</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/e4072c3c-cf32-4992-847e-efdb846e5784">AddConsoleAlias</a>



<a href="https://msdn.microsoft.com/8169708b-83da-47ef-94be-eca3ca7d0a5b">Console Aliases</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/e8514f24-8121-4fad-94bb-c9eedf7a700d">GetConsoleAlias</a>



<a href="https://msdn.microsoft.com/c229de09-cfa6-4829-9c9a-8ff63500eaf4">GetConsoleAliasExes</a>



<a href="https://msdn.microsoft.com/29e49eba-0864-4ed7-af82-1ba639261c40">GetConsoleAliasesLength</a>
 

 

