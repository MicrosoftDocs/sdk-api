---
UID: NF:tlhelp32.Process32Next
title: Process32Next function
author: windows-sdk-content
description: Retrieves information about the next process recorded in a system snapshot.
old-location: toolhelp\process32next.htm
old-project: ToolHelp
ms.assetid: 843a95fd-27ae-4215-83d0-82fc402b82b6
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Process32Next, Process32Next function [ToolHelp], Process32NextW, _win32_process32next, base.process32next, tlhelp32/Process32Next, tlhelp32/Process32NextW, toolhelp.process32next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tlhelp32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: Process32NextW (Unicode) and Process32Next (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TpcGetSamplesArgs
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-toolhelp-l1-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
-	API-MS-Win-Core-ToolHelp-L1-1-1.dll
api_name:
-	Process32Next
-	Process32Next
-	Process32NextW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# Process32Next function


## -description


Retrieves information about the next process recorded in a system snapshot.


## -parameters




### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a> function.


### -param lppe [out]

A pointer to a 
<a href="https://msdn.microsoft.com/9e2f7345-52bf-4bfc-9761-90b0b374c727">PROCESSENTRY32</a> structure.


## -returns



Returns <b>TRUE</b> if the next entry of the process list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function if no processes exist or the snapshot does not contain process information.




## -remarks



To retrieve information about the first process recorded in a snapshot, use the 
<a href="https://msdn.microsoft.com/097790e8-30c2-4b00-9256-fa26e2ceb893">Process32First</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/318d166f-858f-4f33-9422-977e0c4beb3f">Taking a Snapshot and Viewing Processes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a>



<a href="https://msdn.microsoft.com/9e2f7345-52bf-4bfc-9761-90b0b374c727">PROCESSENTRY32</a>



<a href="https://msdn.microsoft.com/4fb55763-2206-48ad-8b1f-ed2c33b6f56b">Process Walking</a>



<a href="https://msdn.microsoft.com/097790e8-30c2-4b00-9256-fa26e2ceb893">Process32First</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

