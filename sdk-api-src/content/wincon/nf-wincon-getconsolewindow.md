---
UID: NF:wincon.GetConsoleWindow
title: GetConsoleWindow function
author: windows-driver-content
description: Retrieves the window handle used by the console associated with the calling process.
old-location: consoles\getconsolewindow.htm
old-project: consoles
ms.assetid: a5ab0b37-45ac-4413-b6ff-73876556ad38
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleWindow, GetConsoleWindow function [Consoles], _win32_getconsolewindow, base.getconsolewindow, consoles.getconsolewindow, wincon/GetConsoleWindow
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
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
-	API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	GetConsoleWindow
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleWindow function


## -description


Retrieves the window handle used by the console associated with the calling process.


## -parameters






## -returns



The return value is a handle to the window used by the console associated with the calling process or <b>NULL</b> if there is no such associated console.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>
 

 

