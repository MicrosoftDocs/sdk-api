---
UID: NF:memoryapi.MapViewOfFileEx
title: MapViewOfFileEx function (memoryapi.h)
description: Maps a view of a file mapping into the address space of a calling process. A caller can optionally specify a suggested base memory address for the view.
helpviewer_keywords: ["FILE_MAP_ALL_ACCESS","FILE_MAP_COPY","FILE_MAP_EXECUTE","FILE_MAP_LARGE_PAGES","FILE_MAP_READ","FILE_MAP_TARGETS_INVALID","FILE_MAP_WRITE","MapViewOfFileEx","MapViewOfFileEx function","_win32_mapviewoffileex","base.mapviewoffileex","fs.mapviewoffileex","winbase/MapViewOfFileEx"]
old-location: base\mapviewoffileex.htm
tech.root: base
ms.assetid: 2ac8a7d6-5c52-41de-acb9-d7f975fd2a94
ms.date: 10/30/2024
ms.keywords: FILE_MAP_ALL_ACCESS, FILE_MAP_COPY, FILE_MAP_EXECUTE, FILE_MAP_LARGE_PAGES, FILE_MAP_READ, FILE_MAP_TARGETS_INVALID, FILE_MAP_WRITE, MapViewOfFileEx, MapViewOfFileEx function, _win32_mapviewoffileex, base.mapviewoffileex, fs.mapviewoffileex, winbase/MapViewOfFileEx
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
 - MapViewOfFileEx
 - memoryapi/MapViewOfFileEx
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
 - MapViewOfFileEx
---

# MapViewOfFileEx function


## -description

Maps a view of a file mapping into the address space of a calling process. A caller can optionally 
    specify a suggested base memory address for the view.

To specify the NUMA node for the physical memory, see 
    <a href="/windows/desktop/api/winbase/nf-winbase-mapviewoffileexnuma">MapViewOfFileExNuma</a>.

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
A read/write view of the file is mapped.  The file mapping object must have been created with 
         <b>PAGE_READWRITE</b> or <b>PAGE_EXECUTE_READWRITE</b> protection.

When used with the <b>MapViewOfFileEx</b> function, 
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

When used with <b>MapViewOfFileEx</b>, 
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
<td width="40%"><a id="FILE_MAP_LARGE_PAGES"></a><a id="file_map_large_pages"></a><dl>
<dt><b>FILE_MAP_LARGE_PAGES</b></dt>
</dl>
</td>
<td width="60%">
Starting with Windows 10, version 1703, this flag specifies that the view should be mapped using <a href="/windows/desktop/Memory/large-page-support">large page support</a>. The size of the view must be a multiple of the size of a 
         large page reported by the 
         <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getlargepageminimum">GetLargePageMinimum</a> function, and the file-mapping object must have been created using the <b>SEC_LARGE_PAGES</b> option. If you provide a non-null value for <i>lpBaseAddress</i>, then the value must be a multiple of <b>GetLargePageMinimum</b>.

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
<td width="40%"><a id="FILE_MAP_TARGETS_INVALID"></a><a id="file_map_targets_invalid"></a><dl>
<dt><b>FILE_MAP_TARGETS_INVALID</b></dt>
</dl>
</td>
<td width="60%">
Sets all the locations in the mapped file as invalid targets for Control Flow Guard (CFG). This flag is similar to <b>PAGE_TARGETS_INVALID</b>. Use this flag in combination with the execute access right <b>FILE_MAP_EXECUTE</b>. Any indirect call to locations in those pages will fail CFG checks, and the process will be terminated. The default behavior for executable pages allocated is to be marked valid call targets for CFG.

</td>
</tr>
</table>
 

For file-mapping objects created with the <b>SEC_IMAGE</b> attribute, the 
       <i>dwDesiredAccess</i> parameter has no effect, and should be set to any valid value such as 
       <b>FILE_MAP_READ</b>.

For more information  about access to file mapping objects, see 
       <a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File Mapping Security and Access Rights</a>.

### -param dwFileOffsetHigh [in]

The high-order <b>DWORD</b> of the file offset where the view is to begin.

### -param dwFileOffsetLow [in]

The low-order <b>DWORD</b> of the file offset where the view is to begin. The 
      combination of the high and low offsets must specify an offset within the file mapping. They must also match the 
      memory allocation granularity of the system. That is, the offset must be a multiple of the allocation 
      granularity. To obtain the memory allocation granularity of the system, use the 
      <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function, which fills in the members of 
      a <a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a> structure.

### -param dwNumberOfBytesToMap [in]

The number of bytes of a file mapping to map to a view. All bytes must be within the maximum size specified 
      by <a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>. If this parameter is 0 
      (zero), the mapping extends from the specified offset to the end of the file mapping.

### -param lpBaseAddress [in, optional]

A pointer to the memory address in the calling process address space where mapping begins. This must be a 
       multiple of the system's memory allocation granularity, or the function fails. To determine the memory 
       allocation granularity of the system, use the 
       <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function. If there is not enough 
       address space at the specified address, the function fails.

If <i>lpBaseAddress</i> is <b>NULL</b>, the operating system chooses 
       the mapping address. In this scenario, the function is equivalent to the 
       <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> function.

While it is possible to specify an address that is safe now (not used by the operating system), there is no 
       guarantee that the address will remain safe over time. Therefore, it is better to let the operating system 
       choose the address. In this case, you would not store pointers in the memory mapped file, you would store 
       offsets from the base of the file mapping so that the mapping can be used at any address.

## -returns

If the function succeeds, the return value is the starting address of the mapped view.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Mapping a file makes the specified portion of the file visible in the address space of the calling 
    process.

For files that are larger than the address space, you can only map a small portion of the file data at one 
    time. When the first view is complete, then you unmap it and map a new view.

To obtain the size of a view, use the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex">VirtualQueryEx</a> function.

The initial contents of the pages in a file mapping object backed by the page file are 0 (zero).

Typically, the suggested address is used to specify that a file should be mapped at the same address in 
    multiple processes. This requires the region of address space to be available in all involved processes. No other 
    memory allocation can take place in the region that is used for mapping, including the use of the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> or 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualallocex">VirtualAllocEx</a> function to reserve memory.

If the <i>lpBaseAddress</i> parameter specifies a base offset, the function succeeds if the 
     specified memory region is not already in use by the calling process. The system does not ensure that the same 
     memory region is available for the memory mapped file in other 32-bit processes.

Multiple views of a file (or a file mapping object and its mapped file) are <i>coherent</i> 
    if they contain identical data at a specified time. This occurs if the file views are derived from the same file 
    mapping object. A process can duplicate a file mapping object handle into another process by using the 
    <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function, or another process can open 
    a file mapping object by name by using the 
    <a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a> function.

With one important exception, file views derived from any file mapping object that is backed by the same file 
    are coherent or identical at a specific time. Coherency is guaranteed for views within a process and for views 
    that are mapped by different processes.

The exception is related to remote files. Although 
    <b>MapViewOfFileEx</b> works with remote files, it does not 
    keep them coherent. For example, if two computers both map a file as writable, and both change the same page, each 
    computer only sees its own writes to the page. When the data gets updated on the disk, it is not merged.

A mapped view of a file is not guaranteed to be coherent with a file being accessed by the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> or 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> function.

To guard against <b>EXCEPTION_IN_PAGE_ERROR</b> exceptions, use structured exception 
    handling to protect any code that writes to or reads from a memory mapped view of a file other than the page file. 
    For more information, see 
    <a href="/windows/desktop/Memory/reading-and-writing-from-a-file-view">Reading and Writing From a File View</a>.

When modifying a file through a mapped view, the last modification timestamp may not be updated automatically. 
     If required, the caller should use <a href="/windows/desktop/api/fileapi/nf-fileapi-setfiletime">SetFileTime</a> to set the 
     timestamp.

To have a file with executable permissions, an application must call
    <a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> with either 
    <b>PAGE_EXECUTE_READWRITE</b> or <b>PAGE_EXECUTE_READ</b>, and then call 
    <b>MapViewOfFileEx</b> with 
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

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>



<a href="/windows/desktop/Memory/creating-a-file-view">Creating a File View</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/Memory/memory-management-functions">File Mapping Functions</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>



<a href="/windows/desktop/api/winbase/nf-winbase-mapviewoffileexnuma">MapViewOfFileExNuma</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>