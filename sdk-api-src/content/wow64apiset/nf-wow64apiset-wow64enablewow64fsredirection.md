---
UID: NF:wow64apiset.Wow64EnableWow64FsRedirection
tech.root: fs
title: Wow64EnableWow64FsRedirection
ms.assetid: 8d11a7ba-540d-4bd0-881a-a61605357dd8
ms.date: 04/12/2022
ms.keywords: Wow64EnableWow64FsRedirection, Wow64EnableWow64FsRedirection function [Files], base.wow64enablewow64fsredirection, fs.wow64enablewow64fsredirection, wow64apiset/Wow64EnableWow64FsRedirection
targetos: Windows
description: Enables or disables file system redirection for the calling thread.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: wow64apiset.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-wow64-l1-1-3.dll
 - api-ms-win-core-wow64-l1-1-2.dll
 - api-ms-win-core-wow64-l1-1-1.dll
 - api-ms-win-core-wow64-l1-1-0.dll
 - api-ms-win-core-kernel32-private-l1-1-2.dll
 - api-ms-win-core-kernel32-private-l1-1-1.dll
 - api-ms-win-core-kernel32-private-l1-1-0.dll
 - wow64apiset.h
api_name:
 - Wow64EnableWow64FsRedirection
f1_keywords:
 - Wow64EnableWow64FsRedirection
 - wow64apiset/Wow64EnableWow64FsRedirection
dev_langs:
 - c++
helpviewer_keywords:
 - Wow64EnableWow64FsRedirection
---

# Wow64EnableWow64FsRedirection function

## -description

Enables or disables file system redirection for the calling thread.

This function may not work reliably when there are nested calls. Therefore, this function has been replaced by
    the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a> and
    <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a>
    functions.
<div class="alert"><b>Note</b>  These two methods of controlling file system redirection cannot be combined in any way. Do not use the
    <b>Wow64EnableWow64FsRedirection</b>
    function with either the
    <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a> or the
    <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a>
    function.</div><div> </div>

## -parameters

### -param Wow64FsEnableRedirection

Indicates the type of request for WOW64 system folder redirection. If
      <b>TRUE</b>, requests redirection be enabled; if <b>FALSE</b>, requests
      redirection be disabled.

## -returns

Boolean value indicating whether the function succeeded. If <b>TRUE</b>, the function
      succeeded; if <b>FALSE</b>, the function failed.

## -remarks

This function is useful for 32-bit applications that want to gain access to the native system32 directory. By
    default, WOW64 file system redirection is enabled.

<div class="alert"><b>Note</b>  The
     <b>Wow64EnableWow64FsRedirection</b>
     function affects all file operations performed by the current thread, which can have unintended consequences if
     file system redirection is disabled for any length of time. For example, DLL loading depends on file system
     redirection, so disabling file system redirection will cause DLL loading to fail. Also, many feature
     implementations use delayed loading and will fail while redirection is disabled. The failure state of the initial
     delay-load operation is persisted, so any subsequent use of the delay-load function will fail even after file
     system redirection is re-enabled. To avoid these problems, disable file system redirection immediately before
     calls to specific file I/O functions (such as <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>)
     that must not be redirected, and re-enable file system redirection immediately afterward using
     <code>Wow64EnableWow64FsRedirection(TRUE)</code>.</div>
<div> </div>
File redirection is enabled or disabled only for the thread calling this function. This affects only
    operations made by the current thread. Some functions, such as
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

### Examples

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

  //  Disable redirection immediately prior to the native API
  //  function call.
  if( Wow64EnableWow64FsRedirection(FALSE) ) 
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
    if ( FALSE == Wow64EnableWow64FsRedirection(TRUE) )
     {
      //  Failure to re-enable redirection should be considered
      //  a critical failure and execution aborted.
      return;
     }
   }
    
  // The handle, if valid, can be used as usual without
  // leaving redirection disabled.
 
  if( INVALID_HANDLE_VALUE != hFile )  
   {
    // Use the file handle
   }
 }

```

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>

<a href="/windows/desktop/WinProg64/file-system-redirector">File System Redirector</a>

<a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya">GetSystemWow64Directory</a>

<a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64disablewow64fsredirection">Wow64DisableWow64FsRedirection</a>

<a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-wow64revertwow64fsredirection">Wow64RevertWow64FsRedirection</a>
