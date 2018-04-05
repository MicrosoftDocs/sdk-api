---
UID: NF:wincon.SetConsoleHistoryInfo
title: SetConsoleHistoryInfo function
author: windows-driver-content
description: Sets the history settings for the calling process's console.
old-location: consoles\setconsolehistoryinfo.htm
old-project: consoles
ms.assetid: db180f53-aa3c-4a91-bc3e-9f3f0bb7ab01
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleHistoryInfo, SetConsoleHistoryInfo function [Consoles], base.setconsolehistoryinfo, consoleapi3/SetConsoleHistoryInfo, consoles.setconsolehistoryinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Wincon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	SetConsoleHistoryInfo
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleHistoryInfo function


## -description


Sets the history settings for the calling process's console.


## -parameters




### -param lpConsoleHistoryInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/df7d2f12-5299-47ed-b1f6-2db903dba81b">CONSOLE_HISTORY_INFO</a> structure that contains the history settings for the process's console.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the calling process is not a console process, the function fails and sets the last error code to <b>ERROR_ACCESS_DENIED</b>.




## -see-also




<a href="https://msdn.microsoft.com/df7d2f12-5299-47ed-b1f6-2db903dba81b">CONSOLE_HISTORY_INFO</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/145008b3-8a4a-4e6a-9144-ee787ce90ef4">GetConsoleHistoryInfo</a>
 

 

