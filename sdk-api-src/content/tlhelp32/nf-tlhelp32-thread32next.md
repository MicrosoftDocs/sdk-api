---
UID: NF:tlhelp32.Thread32Next
title: Thread32Next function
author: windows-sdk-content
description: Retrieves information about the next thread of any process encountered in the system memory snapshot.
old-location: toolhelp\thread32next.htm
tech.root: ToolHelp
ms.assetid: 5efe514e-626c-4138-97a0-bdad217c424f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Thread32Next, Thread32Next function [ToolHelp], _win32_thread32next, base.thread32next, tlhelp32/Thread32Next, toolhelp.thread32next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tlhelp32.h
req.include-header: 
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-toolhelp-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-ToolHelp-L1-1-1.dll
api_name:
 - Thread32Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Thread32Next function


## -description


Retrieves information about the next thread of any process encountered in the system memory snapshot.


## -parameters




### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a> function.


### -param lpte [out]

A pointer to a 
<a href="https://msdn.microsoft.com/923feca1-8807-4752-8a5a-79075688aabd">THREADENTRY32</a> structure.


## -returns



Returns <b>TRUE</b> if the next entry of the thread list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function if no threads exist or the snapshot does not contain thread information.




## -remarks



To retrieve information about the first thread recorded in a snapshot, use the 
<a href="https://msdn.microsoft.com/d4cb7a19-850e-43b5-bda5-91be48382d2a">Thread32First</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/67194627-8239-46d2-93e7-eb8e5f6c56e6">Traversing the Thread List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/df643c25-7558-424c-b187-b3f86ba51358">CreateToolhelp32Snapshot</a>



<a href="https://msdn.microsoft.com/923feca1-8807-4752-8a5a-79075688aabd">THREADENTRY32</a>



<a href="https://msdn.microsoft.com/2440b781-652d-4d73-b173-87504e7b49b5">Thread Walking</a>



<a href="https://msdn.microsoft.com/d4cb7a19-850e-43b5-bda5-91be48382d2a">Thread32First</a>



<a href="https://msdn.microsoft.com/83732bd6-f4cf-409d-ad17-86503d408dc3">Tool Help Functions</a>
 

 

