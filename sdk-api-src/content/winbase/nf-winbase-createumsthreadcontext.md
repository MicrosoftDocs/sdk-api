---
UID: NF:winbase.CreateUmsThreadContext
title: CreateUmsThreadContext function
author: windows-sdk-content
description: Creates a user-mode scheduling (UMS) thread context to represent a UMS worker thread.
old-location: base\createumsthreadcontext.htm
old-project: procthread
ms.assetid: b27ce81a-8463-46af-8acf-2de091f625df
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: CreateUmsThreadContext, CreateUmsThreadContext function, base.createumsthreadcontext, winbase/CreateUmsThreadContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - CreateUmsThreadContext
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateUmsThreadContext function


## -description


Creates a user-mode scheduling (UMS) thread context to represent a UMS worker thread.


## -parameters




### -param lpUmsThread [out]

A PUMS_CONTEXT variable. On output, this parameter receives a pointer to a UMS thread context.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to create the UMS thread context.

</td>
</tr>
</table>
 




## -remarks



A UMS thread context represents the state of a UMS worker thread. Thread contexts are used to specify UMS worker threads in function calls. 

A UMS worker thread is created by calling the <a href="https://msdn.microsoft.com/9c2d9e20-7614-4010-9b8b-4f0e9bc2e6fe">CreateRemoteThreadEx</a> function after using <a href="https://msdn.microsoft.com/58ce70a1-5b73-429f-a062-bacd9b9c5bc8">InitializeProcThreadAttributeList</a> and <a href="https://msdn.microsoft.com/5fc3e04f-9b2a-440c-a9aa-d78d9b25b341">UpdateProcThreadAttribute</a> to prepare a list of UMS attributes for the thread. 

The underlying structures for a UMS thread context are managed by the system and should not be modified directly. To get and set information about a UMS worker thread, use the <a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a> and <a href="https://msdn.microsoft.com/19f190fd-1f78-4bb6-93eb-73a5c522b44d">SetUmsThreadInformation</a> functions.

After a UMS worker thread terminates, its thread context should be released by calling <a href="https://msdn.microsoft.com/cdd118fc-f664-44ce-958d-857216ceb9a7">DeleteUmsThreadContext</a>. 




## -see-also




<a href="https://msdn.microsoft.com/9c2d9e20-7614-4010-9b8b-4f0e9bc2e6fe">CreateRemoteThreadEx</a>



<a href="https://msdn.microsoft.com/cdd118fc-f664-44ce-958d-857216ceb9a7">DeleteUmsThreadContext</a>



<a href="https://msdn.microsoft.com/58ce70a1-5b73-429f-a062-bacd9b9c5bc8">InitializeProcThreadAttributeList</a>



<a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a>



<a href="https://msdn.microsoft.com/19f190fd-1f78-4bb6-93eb-73a5c522b44d">SetUmsThreadInformation</a>



<a href="https://msdn.microsoft.com/5fc3e04f-9b2a-440c-a9aa-d78d9b25b341">UpdateProcThreadAttribute</a>
 

 

