---
UID: NF:winbase.QueryUmsThreadInformation
title: QueryUmsThreadInformation function
author: windows-sdk-content
description: Retrieves information about the specified user-mode scheduling (UMS) worker thread.
old-location: base\queryumsthreadinformation.htm
old-project: ProcThread
ms.assetid: 5f694edf-ba5e-45a2-a938-5013edddcae2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: QueryUmsThreadInformation, QueryUmsThreadInformation function, base.queryumsthreadinformation, winbase/QueryUmsThreadInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
 - QueryUmsThreadInformation
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# QueryUmsThreadInformation function


## -description


Retrieves information about the specified user-mode scheduling (UMS) worker thread.


## -parameters




### -param UmsThread [in]

A pointer to a UMS thread context. 


### -param UmsThreadInfoClass [in]

A <a href="https://msdn.microsoft.com/2d6730b2-4d01-45f5-9514-0d91806f50d5">UMS_THREAD_INFO_CLASS</a> value that specifies the kind of information to retrieve. 


### -param UmsThreadInformation [out]

A pointer to a buffer to receive the specified information. The required size of this buffer depends on the specified information class.

If the information class is <b>UmsThreadContext</b> or <b>UmsThreadTeb</b>, the buffer must be <code>sizeof(PVOID)</code>.

If the information class is <b>UmsThreadIsSuspended</b> or <b>UmsThreadIsTerminated</b>, the buffer must be <code>sizeof(BOOLEAN)</code>.


### -param UmsThreadInformationLength [in]

The size of the <i>UmsThreadInformation</i> buffer, in bytes. 


### -param ReturnLength [out, optional]

A pointer to a ULONG variable. On output, this parameter receives the number of bytes written to the <i>UmsThreadInformation</i> buffer.


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
<dt><b>ERROR_INFO_LENGTH_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small for the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_INFO_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The specified information class is not supported.

</td>
</tr>
</table>
 




## -remarks



The <b>QueryUmsThreadInformation</b> function retrieves information about the specified UMS worker thread such as its application-defined context, its thread execution block (<a href="https://msdn.microsoft.com/fc77fc09-6319-4daa-ac96-1ded661ef800">TEB</a>), and whether the thread is suspended or terminated. 

The underlying structures for UMS worker threads are managed by the system. Information that is not exposed through <b>QueryUmsThreadInformation</b> should be considered reserved.




## -see-also




<a href="https://msdn.microsoft.com/19f190fd-1f78-4bb6-93eb-73a5c522b44d">SetUmsThreadInformation</a>



<a href="https://msdn.microsoft.com/2d6730b2-4d01-45f5-9514-0d91806f50d5">UMS_THREAD_INFO_CLASS</a>
 

 

