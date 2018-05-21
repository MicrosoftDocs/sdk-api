---
UID: NF:winbase.SetUmsThreadInformation
title: SetUmsThreadInformation function
author: windows-driver-content
description: Sets application-specific context information for the specified user-mode scheduling (UMS) worker thread.
old-location: base\setumsthreadinformation.htm
old-project: ProcThread
ms.assetid: 19f190fd-1f78-4bb6-93eb-73a5c522b44d
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: SetUmsThreadInformation, SetUmsThreadInformation function, base.setumsthreadinformation, winbase/SetUmsThreadInformation
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-ums-l1-1-0.dll
api_name:
-	SetUmsThreadInformation
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetUmsThreadInformation function


## -description


Sets application-specific context information for the specified user-mode scheduling (UMS) worker thread.


## -parameters




### -param UmsThread [in]

A pointer to a UMS thread context. 


### -param UmsThreadInfoClass [in]

A <a href="https://msdn.microsoft.com/2d6730b2-4d01-45f5-9514-0d91806f50d5">UMS_THREAD_INFO_CLASS</a> value that specifies the kind of information to set. This parameter must be <b>UmsThreadUserContext</b>.


### -param UmsThreadInformation [in]

A pointer to a buffer that contains the information to set.


### -param UmsThreadInformationLength [in]

The size of the <i>UmsThreadInformation</i> buffer, in bytes. 


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
The buffer size does not match the  required size for the specified information class. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_INFO_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The <i>UmsThreadInfoClass</i> parameter specifies an information class that is not supported.

</td>
</tr>
</table>
 




## -remarks



The <b>SetUmsThreadInformation</b> function can be used to set an application-defined context for the specified UMS worker thread. The context information can consist of anything the application might find useful to track, such as per-scheduler or per-worker thread state. The underlying structures for UMS worker threads are managed by the system and should not be modified directly. 

The <a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a> function can be used to retrieve other exposed information about the specified thread, such as its thread execution block (<a href="https://msdn.microsoft.com/fc77fc09-6319-4daa-ac96-1ded661ef800">TEB</a>) and whether the thread is suspended or terminated. Information that is not exposed through <b>QueryUmsThreadInformation</b> should be considered reserved.




## -see-also




<a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a>
 

 

