---
UID: NF:memoryapi.MapViewOfFileFromApp
title: MapViewOfFileFromApp function (memoryapi.h)
author: windows-sdk-content
description: Maps a view of a file mapping into the address space of a calling Windows Store app.
old-location: base\mapviewoffilefromapp.htm
tech.root: Memory
ms.assetid: 59369959-3347-44d0-8b08-5c38ac58fdb0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FILE_MAP_ALL_ACCESS, FILE_MAP_COPY, FILE_MAP_LARGE_PAGES, FILE_MAP_READ, FILE_MAP_TARGETS_INVALID, FILE_MAP_WRITE, MapViewOfFileFromApp, MapViewOfFileFromApp function, base.mapviewoffilefromapp, memoryapi/MapViewOfFileFromApp
ms.topic: function
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - MapViewOfFileFromApp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MapViewOfFileFromApp function


## -description


Maps a view of a file mapping into the address space of a calling 
    Windows Store app.


## -parameters




### -param hFileMappingObject [in]

A handle to a file mapping object. The 
       <a href="https://msdn.microsoft.com/ef7ad1aa-2ce7-4a77-a57e-d6e55d58b8d3">CreateFileMappingFromApp</a>  function returns 
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
         <b>PAGE_READONLY</b>, <b>PAGE_READ_EXECUTE</b>, 
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
Starting with Windows 10, version 1703, this flag specifies that the view should be mapped using <a href="https://msdn.microsoft.com/060115af-38d1-499c-b30c-47cd0cf42d20">large page support</a>. The size of the view must be a multiple of the size of a 
         large page reported by the 
         <a href="https://msdn.microsoft.com/ccde687d-ee8f-4668-93c1-a1fece86c2f6">GetLargePageMinimum</a> function, and the file-mapping object must have been created using the <b>SEC_LARGE_PAGES</b> option. If you provide a non-null value for <i>lpBaseAddress</i>, then the value must be a multiple of <b>GetLargePageMinimum</b>.

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
       <a href="https://msdn.microsoft.com/8bbf7c98-ff83-4ed9-8b82-f08dcd31295c">File Mapping Security and Access Rights</a>.


### -param FileOffset [in]

The file offset where the view is to begin. The offset must specify an offset within the file mapping. They 
       must also match the  memory allocation granularity of the system. That is, the offset must be a multiple of the 
       allocation granularity. To obtain the memory allocation granularity of the system, use the 
       <a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a> function, which fills in the members of 
       a <a href="https://msdn.microsoft.com/971293b8-0af0-4bdf-a7d7-6b1bb80a469c">SYSTEM_INFO</a> structure.


### -param NumberOfBytesToMap [in]

The number of bytes of a file mapping to map to the view. All bytes must be within the maximum size specified 
       by <a href="https://msdn.microsoft.com/ef7ad1aa-2ce7-4a77-a57e-d6e55d58b8d3">CreateFileMappingFromApp</a>. If this 
       parameter is 0 (zero), the mapping extends from the specified offset to the end of the file mapping.


## -returns



If the function succeeds, the return value is the starting address of the mapped view.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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




<a href="https://msdn.microsoft.com/d3302183-76a0-47ec-874f-1173db353dfe">CreateFileMapping</a>



<a href="https://msdn.microsoft.com/b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4">Creating a File View</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/f6d745af-729a-494e-90b4-19fe7d97c7af">GetSystemInfo</a>



<a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a>



<a href="https://msdn.microsoft.com/2ac8a7d6-5c52-41de-acb9-d7f975fd2a94">MapViewOfFileEx</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory Management Functions</a>



<a href="https://msdn.microsoft.com/4896144c-78fc-4d21-a302-d9ba66fb2f8a">OpenFileMapping</a>



<a href="https://msdn.microsoft.com/971293b8-0af0-4bdf-a7d7-6b1bb80a469c">SYSTEM_INFO</a>



<a href="https://msdn.microsoft.com/2e9c3174-af48-4fa3-9f6a-fb62b23ed994">UnmapViewOfFile</a>
 

 

