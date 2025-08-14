---
UID: NF:memoryapi.MapViewOfFile
title: MapViewOfFile function (memoryapi.h)
description: Maps a view of a file mapping into the address space of a calling process.
helpviewer_keywords: ["FILE_MAP_ALL_ACCESS","FILE_MAP_COPY","FILE_MAP_EXECUTE","FILE_MAP_LARGE_PAGES","FILE_MAP_READ","FILE_MAP_TARGETS_INVALID","FILE_MAP_WRITE","MapViewOfFile","MapViewOfFile function","_win32_mapviewoffile","base.mapviewoffile","fs.mapviewoffile","winbase/MapViewOfFile"]
old-location: base\mapviewoffile.htm
tech.root: base
ms.assetid: df9f54cd-b2de-4107-a1c5-d5a07045851e
ms.date: 10/30/2024
ms.keywords: FILE_MAP_ALL_ACCESS, FILE_MAP_COPY, FILE_MAP_EXECUTE, FILE_MAP_LARGE_PAGES, FILE_MAP_READ, FILE_MAP_TARGETS_INVALID, FILE_MAP_WRITE, MapViewOfFile, MapViewOfFile function, _win32_mapviewoffile, base.mapviewoffile, fs.mapviewoffile, winbase/MapViewOfFile
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MapViewOfFile
 - memoryapi/MapViewOfFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - MapViewOfFile
---

# MapViewOfFile function


## -description

Maps a view of a file mapping into the address space of a calling process.

To specify a suggested base address for the view, use the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a> function. However, this practice is 
    not recommended.

## -parameters

### -param hFileMappingObject [in]

A handle to a file mapping object. The 
       <a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> and 
       <a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a> functions return this handle.

### -param dwDesiredAccess [in]

The type of access to a file mapping object, which determines the page protection of the pages. This 
      parameter can be one of the following values, or a bitwise OR combination of multiple values where appropriate.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_MAP_ALL_ACCESS"></a><a id="file_map_all_access"></a><dl>
<dt><b>FILE_MAP_ALL_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
A read/write view of the file is mapped. The file mapping object must have been created with 
         <b>PAGE_READWRITE</b> or <b>PAGE_EXECUTE_READWRITE</b> protection.

When used with the <b>MapViewOfFile</b> function, 
         <b>FILE_MAP_ALL_ACCESS</b> is equivalent to <b>FILE_MAP_WRITE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_MAP_READ"></a><a id="file_map_read"></a><dl>
<dt><b>FILE_MAP_READ</b></dt>
</dl>
</td>
<td width="60%">
A read-only view of the file is mapped. An attempt to write to the file view results in an access 
         violation.

The file mapping object must have been created with <b>PAGE_READONLY</b>, 
         <b>PAGE_READWRITE</b>, <b>PAGE_EXECUTE_READ</b>, or 
         <b>PAGE_EXECUTE_READWRITE</b> protection.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_MAP_WRITE"></a><a id="file_map_write"></a><dl>
<dt><b>FILE_MAP_WRITE</b></dt>
</dl>
</td>
<td width="60%">
A read/write view of the file is mapped. The file mapping object must have been created with 
         <b>PAGE_READWRITE</b> or <b>PAGE_EXECUTE_READWRITE</b> protection.

When used with <b>MapViewOfFile</b>, 
         (<b>FILE_MAP_WRITE</b> | <b>FILE_MAP_READ</b>) and 
         <b>FILE_MAP_ALL_ACCESS</b> are equivalent to <b>FILE_MAP_WRITE</b>.

</td>
</tr>
</table>
 

Using bitwise OR, you can combine the values above with these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_MAP_COPY"></a><a id="file_map_copy"></a><dl>
<dt><b>FILE_MAP_COPY</b></dt>
</dl>
</td>
<td width="60%">
A copy-on-write view of the file is mapped. The file mapping object must have been created with 
         <b>PAGE_READONLY</b>, <b>PAGE_EXECUTE_READ</b>, 
         <b>PAGE_WRITECOPY</b>, <b>PAGE_EXECUTE_WRITECOPY</b>, 
         <b>PAGE_READWRITE</b>, or <b>PAGE_EXECUTE_READWRITE</b> protection.

When a process writes to a copy-on-write page, the system copies the original page to a new page that is 
         private to the process. The new page is backed by the paging file. The protection of the new page changes 
         from copy-on-write to read/write.

When copy-on-write access is specified, the system and process commit charge taken is for the entire view 
         because the calling process can potentially write to every page in the view, making all pages private. The 
         contents of the new page are never written back to the original file and are lost when the view is 
         unmapped.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_MAP_EXECUTE"></a><a id="file_map_execute"></a><dl>
<dt><b>FILE_MAP_EXECUTE</b></dt>
</dl>
</td>
<td width="60%">
An executable view of the file is mapped (mapped memory can be run as code). The file mapping object must 
         have been created with <b>PAGE_EXECUTE_READ</b>, 
         <b>PAGE_EXECUTE_WRITECOPY</b>, or <b>PAGE_EXECUTE_READWRITE</b> 
         protection.

<b>Windows Server 2003 and Windows XP:  </b>This value is available starting with Windows XP with SP2 and 
          Windows Server 2003 with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_MAP_LARGE_PAGES"></a><a id="file_map_large_pages"></a><dl>
<dt><b>FILE_MAP_LARGE_PAGES</b></dt>
</dl>
</td>
<td width="60%">
Starting with Windows 10, version 1703, this flag specifies that the view should be mapped using <a href="/windows/desktop/Memory/large-page-support">large page support</a>. The size of the view must be a multiple of the size of a large page reported by the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getlargepageminimum">GetLargePageMinimum</a> function, and the file-mapping object must have been created using the <b>SEC_LARGE_PAGES</b> option. If you provide a non-null value for <i>lpBaseAddress</i>, then the value must be a multiple of <b>GetLargePageMinimum</b>.<br/><br/><b>Note: </b>On OS versions before Windows 10, version 1703, the <b>FILE_MAP_LARGE_PAGES</b> flag has no effect. On these releases, the view is automatically mapped using large pages if the section was created with the <b>SEC_LARGE_PAGES</b> flag set.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_MAP_TARGETS_INVALID"></a><a id="file_map_targets_invalid"></a><dl>
<dt><b>FILE_MAP_TARGETS_INVALID</b></dt>
</dl>
</td>
<td width="60%">
Sets all the locations in the mapped file as invalid targets for Control Flow Guard (CFG). This flag is similar to <b>PAGE_TARGETS_INVALID</b>. Use this flag in combination with the execute access right <b>FILE_MAP_EXECUTE</b>. Any indirect call to locations in those pages will fail CFG checks, and the process will be terminated. The default behavior for executable pages allocated is to be marked valid call targets for CFG.

</td>
</tr>
</table>
 

For file mapping objects created with the <b>SEC_IMAGE</b> attribute, the 
       <i>dwDesiredAccess</i> parameter has no effect, and should be set to any valid value such as 
       <b>FILE_MAP_READ</b>.

For more information  about access to file mapping objects, see 
       <a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File Mapping Security and Access Rights</a>.

### -param dwFileOffsetHigh [in]

A high-order <b>DWORD</b> of the file offset where the view begins.

### -param dwFileOffsetLow [in]

A low-order <b>DWORD</b> of the file offset where the view is to begin. The combination 
       of the high and low offsets must specify an offset within the file mapping. They must also match the virtual memory 
       allocation granularity of the system. That is, the offset must be a multiple of the VirtualAlloc allocation granularity. To 
       obtain the VirtualAlloc memory allocation granularity of the system, use the 
       <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function, which fills in the members of 
       a <a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a> structure.

### -param dwNumberOfBytesToMap [in]

The number of bytes of a file mapping to map to the view. All bytes must be within the maximum size specified 
       by <a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>. If this parameter is 0 
       (zero), the mapping extends from the specified offset to the end of the file mapping.

## -returns

If the function succeeds, the return value is the starting address of the mapped view.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Mapping a file makes the specified portion of a file visible in the address space of the calling process.

For files that are larger than the address space, you can only map a small portion of the file data at one 
    time. When the first view is complete, you can unmap it and map a new view.

To obtain the size of a view, use the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a> 
    function.

Multiple views of a file (or a file mapping object and its mapped file) are <i>coherent</i> 
    if they contain identical data at a specified time. This occurs if the file views are derived from any file 
    mapping object that is backed by the same file. A process can duplicate a file mapping object handle into another 
    process by using the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function, or 
    another process can open a file mapping object by name by using the 
    <a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a> function.

With one important exception, file views derived from any file mapping object that is backed by the same file 
    are coherent or identical at a specific time. Coherency is guaranteed for views within a process and for views 
    that are mapped by different processes.

The exception is related to remote files. Although 
    <b>MapViewOfFile</b> works with remote files, it does not keep 
    them coherent. For example, if two computers both map a file as writable, and both change the same page, each 
    computer only sees its own writes to the page. When the data gets updated on the disk, it is not merged.

A mapped view of a file is not guaranteed to be coherent with a file that is being accessed by the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> or 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> function.

Do not store pointers in the memory mapped file; store offsets from the base of the file mapping so that the 
    mapping can be used at any address.

To guard against <b>EXCEPTION_IN_PAGE_ERROR</b> 
    exceptions, use structured exception handling to protect any code that writes to or reads from a memory mapped 
    view of a file other than the page file. For more information, see 
    <a href="/windows/desktop/Memory/reading-and-writing-from-a-file-view">Reading and Writing From a File View</a>.

When modifying a file through a mapped view, the last modification timestamp may not be updated automatically. 
     If required, the caller should use <a href="/windows/desktop/api/fileapi/nf-fileapi-setfiletime">SetFileTime</a> to set the 
     timestamp.

If a file mapping object is backed by the paging file 
     (<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> is called with the 
     <i>hFile</i> parameter set to <b>INVALID_HANDLE_VALUE</b>), the paging file 
     must be large enough to hold the entire mapping. If it is not, 
     <b>MapViewOfFile</b> fails. The initial contents of the pages 
     in a file mapping object backed by the paging file are 0 (zero).

When a file mapping object that is backed by the paging file is created, the caller can  specify whether 
     <b>MapViewOfFile</b> should reserve and commit pages at the 
     same time (<b>SEC_COMMIT</b>) or  simply reserve pages 
     (<b>SEC_RESERVE</b>). Mapping the file makes the entire mapped virtual address range 
     unavailable to other allocations in the process. After a page from the reserved range is committed, it cannot be 
     freed or decommitted by calling <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a>. Reserved and 
     committed pages are released when the view is unmapped and the file mapping object is closed. For details, see 
     the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a> and 
     <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> functions.

To have a file with executable permissions, an application must call 
     <a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> with either 
     <b>PAGE_EXECUTE_READWRITE</b> or <b>PAGE_EXECUTE_READ</b>, 
     and then call <b>MapViewOfFile</b> with 
     <b>FILE_MAP_EXECUTE</b> | <b>FILE_MAP_WRITE</b> or 
     <b>FILE_MAP_EXECUTE</b> | <b>FILE_MAP_READ</b>.

In Windows Server 2012, this function is supported by the following technologies.

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
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

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
Yes

</td>
</tr>
</table>
 

When CsvFs is paused this call might fail with an error indicating that there is a lock conflict.


#### Examples

For an example, see 
     <a href="/windows/desktop/Memory/creating-named-shared-memory">Creating Named Shared Memory</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>



<a href="/windows/desktop/Memory/creating-a-file-view">Creating a File View</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a>



<a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a>
