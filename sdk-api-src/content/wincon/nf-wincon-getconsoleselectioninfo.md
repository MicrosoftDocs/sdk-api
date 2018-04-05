---
UID: NF:wincon.GetConsoleSelectionInfo
title: GetConsoleSelectionInfo function
author: windows-driver-content
description: Retrieves information about the current console selection.
old-location: consoles\getconsoleselectioninfo.htm
old-project: consoles
ms.assetid: 912efe9d-75dd-43bd-8dca-08671b5ed79c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleSelectionInfo, GetConsoleSelectionInfo function [Consoles], _win32_getconsoleselectioninfo, base.getconsoleselectioninfo, consoles.getconsoleselectioninfo, wincon/GetConsoleSelectionInfo
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
-	GetConsoleSelectionInfo
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleSelectionInfo function


## -description


Retrieves information about the current console selection.


## -parameters




### -param lpConsoleSelectionInfo [out]

A pointer to a 
<a href="https://msdn.microsoft.com/9530b249-8db4-4516-9cc8-2b452c6751f9">CONSOLE_SELECTION_INFO</a> structure that receives the selection information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/9530b249-8db4-4516-9cc8-2b452c6751f9">CONSOLE_SELECTION_INFO</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/2f631e1b-d502-45b7-9c15-34c01e913738">Console Selection</a>
 

 

