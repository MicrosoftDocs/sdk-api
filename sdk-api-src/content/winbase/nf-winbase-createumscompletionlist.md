---
UID: NF:winbase.CreateUmsCompletionList
title: CreateUmsCompletionList function (winbase.h)
description: Creates a user-mode scheduling (UMS) completion list.
helpviewer_keywords: ["CreateUmsCompletionList","CreateUmsCompletionList function","base.createumscompletionlist","winbase/CreateUmsCompletionList"]
old-location: base\createumscompletionlist.htm
tech.root: backup
ms.assetid: 6e77b793-a82e-4e23-8c8b-7aff79d69346
ms.date: 12/05/2018
ms.keywords: CreateUmsCompletionList, CreateUmsCompletionList function, base.createumscompletionlist, winbase/CreateUmsCompletionList
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateUmsCompletionList
 - winbase/CreateUmsCompletionList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - CreateUmsCompletionList
req.apiset: api-ms-win-core-ums-l1-1-0 (introduced in Windows 7)
---

# CreateUmsCompletionList function


## -description

Creates a user-mode scheduling (UMS) completion list.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -parameters

### -param UmsCompletionList [out]

A <b>PUMS_COMPLETION_LIST</b> variable. On output, this parameter receives a pointer 
      to an empty UMS completion list.

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include the 
       following.

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
Not enough memory is available to create the completion list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">UMS is not supported.</td>
</tr>
</table>

## -remarks

A completion list is associated with a UMS scheduler thread when the 
    <a href="/windows/desktop/api/winbase/nf-winbase-enterumsschedulingmode">EnterUmsSchedulingMode</a> function is called to 
     create the scheduler thread. The system queues newly created UMS worker threads to the completion list. It also 
     queues previously blocked UMS worker threads to the completion list when the threads are no longer blocked.

When an application's <a href="/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a> entry 
     point function is called, the application's scheduler should retrieve items from the completion list by calling 
     <a href="/windows/desktop/api/winbase/nf-winbase-dequeueumscompletionlistitems">DequeueUmsCompletionListItems</a>.

Each completion list has an associated completion list event which is signaled whenever the system queues 
     items to an empty list. Use the 
     <a href="/windows/desktop/api/winbase/nf-winbase-getumscompletionlistevent">GetUmsCompletionListEvent</a> to obtain a 
     handle to the event for a specified completion list.

When a completion list is no longer needed, use the 
     <a href="/windows/desktop/api/winbase/nf-winbase-deleteumscompletionlist">DeleteUmsCompletionList</a> to release the list. 
     The list must be empty before it can be released.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-dequeueumscompletionlistitems">DequeueUmsCompletionListItems</a>



<a href="/windows/desktop/api/winbase/nf-winbase-enterumsschedulingmode">EnterUmsSchedulingMode</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getumscompletionlistevent">GetUmsCompletionListEvent</a>
