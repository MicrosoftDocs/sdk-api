---
UID: NF:wincon.GetConsoleProcessList
title: GetConsoleProcessList function
author: windows-driver-content
description: Retrieves a list of the processes attached to the current console.
old-location: consoles\getconsoleprocesslist.htm
old-project: consoles
ms.assetid: 3d21103b-662d-4393-ae3f-773cd9e4a930
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetConsoleProcessList, GetConsoleProcessList function [Consoles], _win32_getconsoleprocesslist, base.getconsoleprocesslist, consoles.getconsoleprocesslist, wincon/GetConsoleProcessList
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
-	GetConsoleProcessList
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetConsoleProcessList function


## -description


Retrieves a list of the processes attached to the current console.


## -parameters




### -param lpdwProcessList [out]

A pointer to a buffer that receives an array of process identifiers upon success.

The storage for this buffer is allocated from a shared heap for the process that is 64 KB in size. The maximum size of the buffer will depend on heap usage.


### -param dwProcessCount [in]

The maximum number of process identifiers that can be stored in the <i>lpdwProcessList</i> buffer.


## -returns



If the function succeeds, the return value is less than or equal to <i>dwProcessCount</i> and represents the number of process identifiers stored in the <i>lpdwProcessList</i> buffer.

If the buffer is too small to hold all the valid process identifiers, the return value is the required number of array elements. The function will have stored no identifiers in the buffer. In this situation, use the return value to allocate a buffer that is large enough to store the entire list and call the function again.

If the return value is zero, the function has failed, because every console has at least one process associated with it. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/c00691c3-5878-4a06-9bf3-6073326f36c4">AttachConsole</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>
 

 

