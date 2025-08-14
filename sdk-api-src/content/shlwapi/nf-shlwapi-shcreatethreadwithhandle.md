---
UID: NF:shlwapi.SHCreateThreadWithHandle
title: SHCreateThreadWithHandle function (shlwapi.h)
description: Creates a new thread and retrieves its handle.
helpviewer_keywords: ["SHCreateThreadWithHandle","SHCreateThreadWithHandle function [Windows Shell]","_shell_SHCreateThreadWithHandle","shell.SHCreateThreadWithHandle","shlwapi/SHCreateThreadWithHandle"]
old-location: shell\SHCreateThreadWithHandle.htm
tech.root: shell
ms.assetid: 22a3a97a-857f-46b8-a2e0-8f3a14f40322
ms.date: 12/05/2018
ms.keywords: SHCreateThreadWithHandle, SHCreateThreadWithHandle function [Windows Shell], _shell_SHCreateThreadWithHandle, shell.SHCreateThreadWithHandle, shlwapi/SHCreateThreadWithHandle
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateThreadWithHandle
 - shlwapi/SHCreateThreadWithHandle
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
 - SHCreateThreadWithHandle
---

# SHCreateThreadWithHandle function


## -description

Creates a new thread and retrieves its handle.

## -parameters

### -param pfnThreadProc [in]

Type: <b>LPTHREAD_START_ROUTINE</b>

A pointer to an application-defined function of type <a href="/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)">LPTHREAD_START_ROUTINE</a>. If a new thread was successfully created, this application-defined function is called in the context of that thread. <b>SHCreateThreadWithHandle</b> does not wait for the function pointed to by <i>pfnThreadProc</i> to complete before returning to its caller. The return value for the function specified by <i>pfnThreadProc</i> is the exit code of the thread.

### -param pData [in, optional]

Type: <b>void*</b>

A pointer to an optional application-defined data structure that contains initialization data. It is passed to the function pointed to by <i>pfnThreadProc</i> and, optionally, the function pointed to by <i>pfnCallback</i>.

### -param flags [in]

Type: <b>SHCT_FLAGS</b>

Flags that control the behavior of the function; one or more of the <a href="/windows/desktop/shell/ctf">CTF</a> constants.

### -param pfnCallback [in, optional]

Type: <b>LPTHREAD_START_ROUTINE</b>

A pointer to an optional application-defined function of type <a href="/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)">LPTHREAD_START_ROUTINE</a>. This function is called in the context of the created thread before the function pointed to by <i>pfnThreadProc</i> is called. It will also receive <i>pData</i> as its argument. <b>SHCreateThreadWithHandle</b> waits for the function pointed to by <i>pfnCallback</i> to complete before returning to its caller. The return value for the function specified by <i>pfnCallback</i> is ignored.

### -param pHandle [out, optional]

Type: <b>HANDLE*</b>

A pointer to the <b>HANDLE</b> of the created thread. When it is no longer needed, this handle should be closed by calling the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function. This value can be <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the thread is successfully created; otherwise, <b>FALSE</b>

## -remarks

Prior to Windows 7, this function did not have an associated header or library file. To use this function under those earlier operating systems, call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> with the DLL name (Shlwapi.dll) to obtain a module handle. Then call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> with that module handle and a function ordinal of 615 to get the address of this function.

The function pointed to by <i>pfnThreadProc</i> and <i>pfnCallback</i> must take the following form. 

                


```
DWORD WINAPI ThreadProc(LPVOID pData)
{
    ...
}
```


The function name is arbitrary. The <i>pData</i> parameter points to an application-defined data structure with initialization information.


#### Examples

The following code example provides a function pointer prototype typedef for calling <b>SHCreateThreadWithHandle</b> by ordinal and shows how to accomplish such a call.


```cpp
// Define SHCREATETHREADWITHHANDLE as a function pointer to SHCreateThreadWithHandle.
typedef BOOL (STDMETHODCALLTYPE *SHCREATETHREADWITHHANDLE)(LPTHREAD_START_ROUTINE, 
                                                           void *, 
                                                           DWORD, 
                                                           LPTHREAD_START_ROUTINE, 
                                                           HANDLE *);

// CallSHCreateThreadWithHandle is an example function that:
// 1. Accepts parameters for the SHCreateThreadWithHandle function.
// 2. Loads Shlwapi.dll, which implements SHCreateThreadWithHandle.
// 3. Obtains the address of SHCreateThreadWithHandle in the loaded library.
// 4. Calls SHCreateThreadWithHandle through a SHCREATETHREADWITHHANDLE function pointer.

BOOL CallSHCreateThreadWithHandle(LPTHREAD_START_ROUTINE pfnThreadProc, 
                                  void *pData,
                                  DWORD dwFlags, 
                                  LPTHREAD_START_ROUTINE pfnCallback, 
                                  HANDLE *pHandle)
{
    // Build a string that contains the local path to Shlwapi.dll.
    WCHAR szPath[MAX_PATH];
    GetSystemDirectory(szPath, ARRAYSIZE(szPath));  
    PathAppend(szPath, L"shlwapi.dll");

    // Attempt to load Shlwapi.dll.
    HMODULE hModule = LoadLibrary(szPath);

    HRESULT hr = hModule ? S_OK : HRESULT_FROM_WIN32(GetLastError());
    if (SUCCEEDED(hr)) 
    {
        // Shlwapi.dll is loaded. 
        // Before Windows 7, SHCreateThreadWithHandle must be accessed through 
        // its ordinal. The following commented lines are used for this.
        
        // Get the address of SHCreateThreadWithHandle through its ordinal value of 615.
        // SHCREATETHREADWITHHANDLE pfn =
        //     (SHCREATETHREADWITHHANDLE)GetProcAddress(hModule, MAKEINTRESOURCEA(615));
        //
        // hr = pfn ? S_OK : HRESULT_FROM_WIN32(GetLastError());
        //
        // if (SUCCEEDED(hr))
        // {
        //     // Call SHCreateThreadWithHandle through SHCREATETHREADWITHHANDLE.
        //     hr = pfn(pfnThreadProc, pData, dwFlags, pfnCallback, pHandle) 
        //               ? S_OK : HRESULT_FROM_WIN32(GetLastError());
        // }
        // FreeLibrary(hModule);
        
        hr = SHCreateThreadWithHandle(pfnThreadProc, pData, dwFlags, pfnCallback, pHandle) 
                       ? S_OK : HRESULT_FROM_WIN32(GetLastError());
    }
    return SUCCEEDED(hr);
}
```

## -see-also

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a>



<a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>