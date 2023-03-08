---
UID: NF:winbase.DeleteUmsCompletionList
title: DeleteUmsCompletionList function (winbase.h)
description: Deletes the specified user-mode scheduling (UMS) completion list. The list must be empty.
helpviewer_keywords: ["DeleteUmsCompletionList","DeleteUmsCompletionList function","base.deleteumscompletionlist","winbase/DeleteUmsCompletionList"]
old-location: base\deleteumscompletionlist.htm
tech.root: backup
ms.assetid: 98124359-ddd1-468c-9f99-74dd3f631fa1
ms.date: 12/05/2018
ms.keywords: DeleteUmsCompletionList, DeleteUmsCompletionList function, base.deleteumscompletionlist, winbase/DeleteUmsCompletionList
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
 - DeleteUmsCompletionList
 - winbase/DeleteUmsCompletionList
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
 - DeleteUmsCompletionList
req.apiset: api-ms-win-core-ums-l1-1-0 (introduced in Windows 7)
---

# DeleteUmsCompletionList function


## -description

Deletes the specified user-mode scheduling (UMS) completion list. The list must be empty.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -parameters

### -param UmsCompletionList [in]

A pointer to the UMS completion list to be deleted. The <a href="/windows/desktop/api/winbase/nf-winbase-createumscompletionlist">CreateUmsCompletionList</a> function provides this pointer.

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the completion list is shared, the caller is responsible for ensuring that no active UMS thread holds a reference to the list before deleting it.
