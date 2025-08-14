---
UID: NF:wow64apiset.Wow64DisableWow64FsRedirection
title: Wow64DisableWow64FsRedirection function (wow64apiset.h)
description: Disables file system redirection for the calling thread. File system redirection is enabled by default.
helpviewer_keywords: ["Wow64DisableWow64FsRedirection","Wow64DisableWow64FsRedirection function [Files]","base.wow64disablewow64fsredirection","fs.wow64disablewow64fsredirection","wow64apiset/Wow64DisableWow64FsRedirection"]
old-location: fs\wow64disablewow64fsredirection.htm
tech.root: fs
ms.assetid: 44bedfa3-5a92-4e78-9e38-8278a7efe9b7
ms.date: 04/14/2022
ms.keywords: Wow64DisableWow64FsRedirection, Wow64DisableWow64FsRedirection function [Files], base.wow64disablewow64fsredirection, fs.wow64disablewow64fsredirection, wow64apiset/Wow64DisableWow64FsRedirection
req.header: wow64apiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - Wow64DisableWow64FsRedirection
 - wow64apiset/Wow64DisableWow64FsRedirection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-wow64-l1-1-3.dll
 - api-ms-win-core-wow64-l1-1-2.dll
 - Kernel32.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Wow64-l1-1-0.dll
 - API-MS-Win-Core-Wow64-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - Wow64DisableWow64FsRedirection
---

# Wow64DisableWow64FsRedirection function


## -description

Disables file system redirection for the calling thread. File system redirection is enabled by 
    default.

## -parameters

### -param OldValue [out]

The WOW64 file system redirection value. The system uses this parameter to store information necessary to 
       revert (re-enable) file system redirection.

<div class="alert"><b>Note</b>  This value is for system use only. To avoid unpredictable behavior, do not modify this value in any 
       way.</div>
<div> </div>

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is useful for 32-bit applications that want to gain access to the native system32 directory. By 
    default, WOW64 file system redirection is enabled.

The 
    <b>Wow64DisableWow64FsRedirection</b>/<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a> 
    function pairing is a replacement for the functionality of the 
    <a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64enablewow64fsredirection">Wow64EnableWow64FsRedirection</a> 
    function.

To restore file system redirection, call the 
    <a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a> 
    function. Every successful call to the 
    <b>Wow64DisableWow64FsRedirection</b> function 
    must have a matching call to the 
    <b>Wow64RevertWow64FsRedirection</b> 
    function. This will ensure redirection is re-enabled and frees associated system resources.

<div class="alert"><b>Note</b>  The <b>Wow64DisableWow64FsRedirection</b> 
     function affects all file operations performed by the current thread, which can have unintended consequences if 
     file system redirection is disabled for any length of time. For example, DLL loading depends on file system 
     redirection, so disabling file system redirection will cause DLL loading to fail. Also, many feature 
     implementations use delayed loading and will fail while redirection is disabled. The failure state of the initial 
     delay-load operation is persisted, so any subsequent use of the delay-load function will fail even after file 
     system redirection is re-enabled. To avoid these problems, disable file system redirection immediately before 
     calls to specific file I/O functions (such as <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>) 
     that must not be redirected, and re-enable file system redirection immediately afterward using 
     <a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a>.</div>
<div> </div>
Disabling file system redirection affects only operations made by the current thread. Some functions, such as 
    <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>, do their work on another 
    thread, which is not affected by the state of file system redirection in the calling thread.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 


#### Examples

The following example uses 
     <b>Wow64DisableWow64FsRedirection</b> to 
     disable file system redirection so that a 32-bit application that is running under WOW64 can open the 64-bit 
     version of Notepad.exe in %SystemRoot%\System32 instead of being redirected 
     to the 32-bit version in %SystemRoot%\SysWOW64.

```cpp
#ifdef _WIN32_WINNT
#undef _WIN32_WINNT
#endif
#define _WIN32_WINNT 0x0501

#ifdef NTDDI_VERSION
#undef NTDDI_VERSION
#endif
#define NTDDI_VERSION 0x05010000

#include <Windows.h>

void main()
{
    HANDLE hFile = INVALID_HANDLE_VALUE;
    PVOID OldValue = NULL;

    //  Disable redirection immediately prior to the native API
    //  function call.
    if( Wow64DisableWow64FsRedirection(&OldValue) ) 
    {
        //  Any function calls in this block of code should be as concise
        //  and as simple as possible to avoid unintended results.
        hFile = CreateFile(TEXT("C:\\Windows\\System32\\Notepad.exe"),
            GENERIC_READ,
            FILE_SHARE_READ,
            NULL,
            OPEN_EXISTING,
            FILE_ATTRIBUTE_NORMAL,
            NULL);

        //  Immediately re-enable redirection. Note that any resources
        //  associated with OldValue are cleaned up by this call.
        if ( FALSE == Wow64RevertWow64FsRedirection(OldValue) )
        {
            //  Failure to re-enable redirection should be considered
            //  a critical failure and execution aborted.
            return;
        }
    }
    
    //  The handle, if valid, now can be used as usual, and without
    //  leaving redirection disabled. 
    if( INVALID_HANDLE_VALUE != hFile )  
    {
        // Use the file handle
    }
}
```

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>

<a href="/windows/desktop/WinProg64/file-system-redirector">File System Redirector</a>

<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64enablewow64fsredirection">Wow64EnableWow64FsRedirection</a>

<a href="/windows/win32/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a>