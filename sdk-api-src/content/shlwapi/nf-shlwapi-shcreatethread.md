---
UID: NF:shlwapi.SHCreateThread
title: SHCreateThread function (shlwapi.h)
description: Creates a thread.
helpviewer_keywords: ["SHCreateThread","SHCreateThread function [Windows Shell]","_win32_SHCreateThread","shell.SHCreateThread","shlwapi/SHCreateThread"]
old-location: shell\SHCreateThread.htm
tech.root: shell
ms.assetid: 2140e396-29cd-4665-b684-337170570b73
ms.date: 12/05/2018
ms.keywords: SHCreateThread, SHCreateThread function [Windows Shell], _win32_SHCreateThread, shell.SHCreateThread, shlwapi/SHCreateThread
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateThread
 - shlwapi/SHCreateThread
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-shlwapi-l2-1-0.dll
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - ShCore.dll
 - API-MS-Win-ShCore-thread-l1-1-0.dll
api_name:
 - SHCreateThread
---

# SHCreateThread function


## -description

Creates a thread.

## -parameters

### -param pfnThreadProc [in]

Type: <b>LPTHREAD_START_ROUTINE</b>

A pointer to an application-defined function of the <a href="/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)">LPTHREAD_START_ROUTINE</a> type. If a new thread was successfully created, this application-defined function is called in the context of that thread. <b>SHCreateThread</b> does not wait for the function pointed to by this parameter to complete before returning to its caller.  The application-defined function's return value is the exit code of the thread.

### -param pData [in, optional]

Type: <b>void*</b>

A pointer to an optional application-defined data structure that contains initialization data. It is passed to the function pointed to by <i>pfnThreadProc</i> and, optionally, <i>pfnCallback</i>. This value can be <b>NULL</b>.

### -param flags [in]

Type: <b>SHCT_FLAGS</b>

The flags that control the behavior of the function. One or more of the <a href="/windows/desktop/shell/ctf">CTF</a> constants.

### -param pfnCallback [in, optional]

Type: <b>LPTHREAD_START_ROUTINE</b>

A pointer to an optional application-defined function of the 
				 <a href="/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)">LPTHREAD_START_ROUTINE</a> type. This function is called 
				 in the context of the created thread before the function pointed to by 
				 <i>pfnThreadProc</i> is called. It will also receive <i>pData</i> as 
				 its argument. <b>SHCreateThread</b> will wait for the 
				 function pointed to by <i>pfnCallback</i> to return before returning to its caller. The 
				 return value of the function pointed to by <i>pfnCallback</i> is ignored.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the thread is successfully created, or <b>FALSE</b> otherwise. On failure, use <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to retrieve the specific error value as shown here.

                    


```
if (!SHCreateThread(...))
{
    hr = HRESULT_FROM_WIN32( GetLastError() );
}
else
{
    ....
}
```

## -remarks

The function pointed to by <i>pfnThreadProc</i> and <i>pfnCallback</i> must take the following form.

				


```
DWORD WINAPI ThreadProc(LPVOID pData)
{
  ...
}
```


The function name is arbitrary. The <i>pData</i> parameter points to an application-defined data structure with initialization information.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatethreadref">SHCreateThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shgetthreadref">SHGetThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shreleasethreadref">SHReleaseThreadRef</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-shsetthreadref">SHSetThreadRef</a>



<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Shell and Common Controls Versions</a>