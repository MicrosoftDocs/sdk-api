---
UID: NF:wincon.AddConsoleAliasW
title: AddConsoleAliasW function
author: windows-driver-content
description: Defines a console alias for the specified executable.
old-location: consoles\addconsolealias.htm
old-project: consoles
ms.assetid: e4072c3c-cf32-4992-847e-efdb846e5784
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddConsoleAlias, AddConsoleAlias function [Consoles], AddConsoleAliasA, AddConsoleAliasW, base.addconsolealias, consoles.addconsolealias, wincon/AddConsoleAlias, wincon/AddConsoleAliasA, wincon/AddConsoleAliasW
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
req.unicode-ansi: AddConsoleAliasW (Unicode) and AddConsoleAliasA (ANSI)
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
-	AddConsoleAlias
-	AddConsoleAliasA
-	AddConsoleAliasW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# AddConsoleAliasW function


## -description


Defines a console alias for the specified executable.


## -parameters




### -param Source [in]

The console alias to be mapped to the text specified by <i>Target</i>.


### -param Target [in]

The text to be substituted for <i>Source</i>. If this parameter is <b>NULL</b>, then the console alias is removed.


### -param ExeName [in]

The name of the executable file for which the console alias is to be defined.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/8169708b-83da-47ef-94be-eca3ca7d0a5b">Console Aliases</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8169708b-83da-47ef-94be-eca3ca7d0a5b">Console Aliases</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/e8514f24-8121-4fad-94bb-c9eedf7a700d">GetConsoleAlias</a>



<a href="https://msdn.microsoft.com/c229de09-cfa6-4829-9c9a-8ff63500eaf4">GetConsoleAliasExes</a>



<a href="https://msdn.microsoft.com/92eefa4e-ffde-4886-afde-5aecf450b425">GetConsoleAliases</a>
 

 

