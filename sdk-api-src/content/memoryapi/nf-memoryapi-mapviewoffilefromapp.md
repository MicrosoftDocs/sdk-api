---
UID: NF:memoryapi.MapViewOfFileFromApp
title: MapViewOfFileFromApp function (memoryapi.h)
description: Maps a view of a file mapping into the address space of a calling Windows Store app. (MapViewOfFileFromApp)
helpviewer_keywords: ["FILE_MAP_ALL_ACCESS","FILE_MAP_COPY","FILE_MAP_LARGE_PAGES","FILE_MAP_READ","FILE_MAP_TARGETS_INVALID","FILE_MAP_WRITE","MapViewOfFileFromApp","MapViewOfFileFromApp function","base.mapviewoffilefromapp","memoryapi/MapViewOfFileFromApp"]
old-location: base\mapviewoffilefromapp.htm
tech.root: base
ms.assetid: 59369959-3347-44d0-8b08-5c38ac58fdb0
ms.date: 10/30/2024
ms.keywords: FILE_MAP_ALL_ACCESS, FILE_MAP_COPY, FILE_MAP_LARGE_PAGES, FILE_MAP_READ, FILE_MAP_TARGETS_INVALID, FILE_MAP_WRITE, MapViewOfFileFromApp, MapViewOfFileFromApp function, base.mapviewoffilefromapp, memoryapi/MapViewOfFileFromApp
req.header: memoryapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MapViewOfFileFromApp
 - memoryapi/MapViewOfFileFromApp
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
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - MapViewOfFileFromApp
---

# MapViewOfFileFromApp function


## -description

Maps a view of a file mapping into the address space of a calling 
    Windows Store app.

## -parameters

### -param hFileMappingObject [in]

A handle to a file mapping object. The 
       <a href="/windows/desktop/api/memoryapi/nf-memoryapi-createfilemappingfromapp">CreateFileMappingFromApp</a>  function returns 
       this handle.

### -param DesiredAccess [in]

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
         <b>PAGE_READWRITE</b> protection.

When used with <b>MapViewOfFileFromApp</b>, <b>FILE_MAP_ALL_ACCESS</b> is equivalent to 
         <b>FILE_MAP_WRITE</b>.

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
         <b>PAGE_READWRITE</b> protection.

When used with <b>MapViewOfFileFromApp</b>, 
         <code>(FILE_MAP_WRITE | FILE_MAP_READ)</code> is equivalent to <b>FILE_MAP_WRITE</b>.

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
         <b>PAGE_WRITECOPY</b>, or 
         <b>PAGE_READWRITE</b> protection.

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

### -param FileOffset [in]

The file offset where the view is to begin. The offset must specify an offset within the file mapping. They 
       must also match the  memory allocation granularity of the system. That is, the offset must be a multiple of the 
       allocation granularity. To obtain the memory allocation granularity of the system, use the 
       <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a> function, which fills in the members of 
       a <a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a> structure.

### -param NumberOfBytesToMap [in]

The number of bytes of a file mapping to map to the view. All bytes must be within the maximum size specified 
       by <a href="/windows/desktop/api/memoryapi/nf-memoryapi-createfilemappingfromapp">CreateFileMappingFromApp</a>. If this 
       parameter is 0 (zero), the mapping extends from the specified offset to the end of the file mapping.

## -returns

If the function succeeds, the return value is the starting address of the mapped view.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

With one important exception, file views derived from any file mapping object that is backed by the same file 
    are coherent or identical at a specific time. Coherency is guaranteed for views within a process and for views 
    that are mapped by different processes.

The exception is related to remote files. Although 
    <b>MapViewOfFileFromApp</b> works with remote files, it 
    does not keep them coherent. For example, if two computers both map a file as writable, and both change the same 
    page, each computer only sees its own writes to the page. When the data gets updated on the disk, it is not 
    merged.

 You can only successfully request executable protection if your app has the <b>codeGeneration</b> capability.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>



<a href="/windows/desktop/Memory/creating-a-file-view">Creating a File View</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo">GetSystemInfo</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a>



<a href="/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info">SYSTEM_INFO</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a>
