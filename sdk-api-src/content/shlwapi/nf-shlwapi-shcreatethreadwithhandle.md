---
UID: NF:shlwapi.SHCreateThreadWithHandle
title: SHCreateThreadWithHandle function
author: windows-sdk-content
description: Creates a new thread and retrieves its handle.
old-location: shell\SHCreateThreadWithHandle.htm
old-project: shell
ms.assetid: 22a3a97a-857f-46b8-a2e0-8f3a14f40322
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SHCreateThreadWithHandle, SHCreateThreadWithHandle function [Windows Shell], _shell_SHCreateThreadWithHandle, shell.SHCreateThreadWithHandle, shlwapi/SHCreateThreadWithHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - ShCore.dll
 - API-MS-Win-ShCore-thread-l1-1-0.dll
api_name:
 - SHCreateThreadWithHandle
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 6.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHCreateThreadWithHandle function


## -description


Creates a new thread and retrieves its handle.


## -parameters




### -param pfnThreadProc [in]

Type: <b>LPTHREAD_START_ROUTINE</b>

A pointer to an application-defined function of type <a href="https://msdn.microsoft.com/f0dc203f-200e-42f1-940c-24e3fe080175">LPTHREAD_START_ROUTINE</a>. If a new thread was successfully created, this application-defined function is called in the context of that thread. <b>SHCreateThreadWithHandle</b> does not wait for the function pointed to by <i>pfnThreadProc</i> to complete before returning to its caller. The return value for the function specified by <i>pfnThreadProc</i> is the exit code of the thread.


### -param pData [in, optional]

Type: <b>void*</b>

A pointer to an optional application-defined data structure that contains initialization data. It is passed to the function pointed to by <i>pfnThreadProc</i> and, optionally, the function pointed to by <i>pfnCallback</i>.


### -param flags [in]

Type: <b>SHCT_FLAGS</b>

Flags that control the behavior of the function; one or more of the <a href="https://msdn.microsoft.com/66cda866-7a39-4c5a-a795-a4c5c64cbab7">CTF</a> constants.


### -param pfnCallback [in, optional]

Type: <b>LPTHREAD_START_ROUTINE</b>

A pointer to an optional application-defined function of type <a href="https://msdn.microsoft.com/f0dc203f-200e-42f1-940c-24e3fe080175">LPTHREAD_START_ROUTINE</a>. This function is called in the context of the created thread before the function pointed to by <i>pfnThreadProc</i> is called. It will also receive <i>pData</i> as its argument. <b>SHCreateThreadWithHandle</b> waits for the function pointed to by <i>pfnCallback</i> to complete before returning to its caller. The return value for the function specified by <i>pfnCallback</i> is ignored.


### -param pHandle [out, optional]

Type: <b>HANDLE*</b>

A pointer to the <b>HANDLE</b> of the created thread. When it is no longer needed, this handle should be closed by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function. This value can be <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the thread is successfully created; otherwise, <b>FALSE</b>




## -remarks



Prior to Windows 7, this function did not have an associated header or library file. To use this function under those earlier operating systems, call <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> with the DLL name (Shlwapi.dll) to obtain a module handle. Then call <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> with that module handle and a function ordinal of 615 to get the address of this function.

The function pointed to by <i>pfnThreadProc</i> and <i>pfnCallback</i> must take the following form. 

                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>DWORD WINAPI ThreadProc(LPVOID pData)
{
    ...
}</pre>
</td>
</tr>
</table></span></div>
The function name is arbitrary. The <i>pData</i> parameter points to an application-defined data structure with initialization information.


#### Examples

The following code example provides a function pointer prototype typedef for calling <b>SHCreateThreadWithHandle</b> by ordinal and shows how to accomplish such a call.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Define SHCREATETHREADWITHHANDLE as a function pointer to SHCreateThreadWithHandle.
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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>



<a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a>



<a href="com.hresult_from_win32">HRESULT_FROM_WIN32</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>
 

 

