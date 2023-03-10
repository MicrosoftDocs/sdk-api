---
UID: NF:winbase.GetUmsCompletionListEvent
title: GetUmsCompletionListEvent function (winbase.h)
description: Retrieves a handle to the event associated with the specified user-mode scheduling (UMS) completion list.
helpviewer_keywords: ["GetUmsCompletionListEvent","GetUmsCompletionListEvent function","base.getumscompletionlistevent","winbase/GetUmsCompletionListEvent"]
old-location: base\getumscompletionlistevent.htm
tech.root: backup
ms.assetid: 393f6e0a-fbea-4aa0-9c18-f96da18e61e9
ms.date: 12/05/2018
ms.keywords: GetUmsCompletionListEvent, GetUmsCompletionListEvent function, base.getumscompletionlistevent, winbase/GetUmsCompletionListEvent
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
 - GetUmsCompletionListEvent
 - winbase/GetUmsCompletionListEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - GetUmsCompletionListEvent
req.apiset: api-ms-win-core-ums-l1-1-0 (introduced in Windows 7)
---

# GetUmsCompletionListEvent function


## -description

Retrieves a handle to the event associated with the specified user-mode scheduling (UMS) completion list.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -parameters

### -param UmsCompletionList [in]

A pointer to a UMS completion list. The <a href="/windows/desktop/api/winbase/nf-winbase-createumscompletionlist">CreateUmsCompletionList</a> function provides this pointer.

### -param UmsCompletionEvent [in, out]

A pointer to a HANDLE variable. On output, the <i>UmsCompletionEvent</i> parameter is set to a handle to the event associated with the specified completion list.

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The system signals a UMS completion list event when the system queues items to an empty completion list. A completion list event handle can be used with any <a href="/windows/desktop/Sync/wait-functions">wait function</a> that takes a handle to an event. When the event is signaled, an application typically calls <a href="/windows/desktop/api/winbase/nf-winbase-dequeueumscompletionlistitems">DequeueUmsCompletionListItems</a> to retrieve the contents of the completion list. 

The event handle remains valid until its completion list is deleted. Do not use the event handle to wait on a completion list that has been deleted or is in the process of being deleted.

When the handle is no longer needed, use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createumscompletionlist">CreateUmsCompletionList</a>



<a href="/windows/desktop/api/winbase/nf-winbase-dequeueumscompletionlistitems">DequeueUmsCompletionListItems</a>



<a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>
