---
UID: NF:winbase.CreateUmsThreadContext
title: CreateUmsThreadContext function (winbase.h)
description: Creates a user-mode scheduling (UMS) thread context to represent a UMS worker thread.
helpviewer_keywords: ["CreateUmsThreadContext","CreateUmsThreadContext function","base.createumsthreadcontext","winbase/CreateUmsThreadContext"]
old-location: base\createumsthreadcontext.htm
tech.root: backup
ms.assetid: b27ce81a-8463-46af-8acf-2de091f625df
ms.date: 12/05/2018
ms.keywords: CreateUmsThreadContext, CreateUmsThreadContext function, base.createumsthreadcontext, winbase/CreateUmsThreadContext
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
 - CreateUmsThreadContext
 - winbase/CreateUmsThreadContext
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
 - CreateUmsThreadContext
req.apiset: api-ms-win-core-ums-l1-1-0 (introduced in Windows 7)
---

# CreateUmsThreadContext function


## -description

Creates a user-mode scheduling (UMS) thread context to represent a UMS worker thread.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -parameters

### -param lpUmsThread [out]

A PUMS_CONTEXT variable. On output, this parameter receives a pointer to a UMS thread context.

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error values include the following.

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

A UMS worker thread is created by calling the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethreadex">CreateRemoteThreadEx</a> function after using <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute">UpdateProcThreadAttribute</a> to prepare a list of UMS attributes for the thread. 

The underlying structures for a UMS thread context are managed by the system and should not be modified directly. To get and set information about a UMS worker thread, use the <a href="/windows/desktop/api/winbase/nf-winbase-queryumsthreadinformation">QueryUmsThreadInformation</a> and <a href="/windows/desktop/api/winbase/nf-winbase-setumsthreadinformation">SetUmsThreadInformation</a> functions.

After a UMS worker thread terminates, its thread context should be released by calling <a href="/windows/desktop/api/winbase/nf-winbase-deleteumsthreadcontext">DeleteUmsThreadContext</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createremotethreadex">CreateRemoteThreadEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deleteumsthreadcontext">DeleteUmsThreadContext</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a>



<a href="/windows/desktop/api/winbase/nf-winbase-queryumsthreadinformation">QueryUmsThreadInformation</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setumsthreadinformation">SetUmsThreadInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute">UpdateProcThreadAttribute</a>
