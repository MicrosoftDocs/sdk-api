---
UID: NF:memoryapi.CreateFileMappingW
title: CreateFileMappingW function (memoryapi.h)
description: Creates or opens a named or unnamed file mapping object for a specified file. (CreateFileMappingW)
helpviewer_keywords: ["CreateFileMapping","CreateFileMapping function","CreateFileMappingA","CreateFileMappingW","PAGE_EXECUTE_READ","PAGE_EXECUTE_READWRITE","PAGE_EXECUTE_WRITECOPY","PAGE_READONLY","PAGE_READWRITE","PAGE_WRITECOPY","SEC_COMMIT","SEC_IMAGE","SEC_IMAGE_NO_EXECUTE","SEC_LARGE_PAGES","SEC_NOCACHE","SEC_RESERVE","SEC_WRITECOMBINE","_win32_createfilemapping","base.createfilemapping","fs.createfilemapping","winbase/CreateFileMapping","winbase/CreateFileMappingA","winbase/CreateFileMappingW"]
old-location: base\createfilemapping.htm
tech.root: base
ms.assetid: d3302183-76a0-47ec-874f-1173db353dfe
ms.date: 12/05/2018
ms.keywords: CreateFileMapping, CreateFileMapping function, CreateFileMappingA, CreateFileMappingW, PAGE_EXECUTE_READ, PAGE_EXECUTE_READWRITE, PAGE_EXECUTE_WRITECOPY, PAGE_READONLY, PAGE_READWRITE, PAGE_WRITECOPY, SEC_COMMIT, SEC_IMAGE, SEC_IMAGE_NO_EXECUTE, SEC_LARGE_PAGES, SEC_NOCACHE, SEC_RESERVE, SEC_WRITECOMBINE, _win32_createfilemapping, base.createfilemapping, fs.createfilemapping, winbase/CreateFileMapping, winbase/CreateFileMappingA, winbase/CreateFileMappingW
req.header: memoryapi.h
req.include-header: Windows.h, Memoryapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateFileMappingW (Unicode) and CreateFileMappingA (ANSI)
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
 - CreateFileMappingW
 - memoryapi/CreateFileMappingW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-memory-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-memory-l1-1-1.dll
 - API-MS-Win-Core-memory-l1-1-2.dll
 - API-MS-Win-Core-memory-l1-1-3.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
api_name:
 - CreateFileMapping
 - CreateFileMappingA
 - CreateFileMappingW
---

# CreateFileMappingW function


## -description

Creates or opens a named or unnamed file mapping object for a specified file.

To specify the NUMA node for the physical memory, see 
    <a href="/windows/desktop/api/winbase/nf-winbase-createfilemappingnumaa">CreateFileMappingNuma</a>.

## -parameters

### -param hFile [in]

A handle to the file from which to create a file mapping object.

The file must be opened with access rights that are compatible with the protection flags that the 
       <i>flProtect</i> parameter specifies. It is not required, but it is recommended that files 
       you intend to map be opened for exclusive access. For more information, see 
       <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

If <i>hFile</i> is <b>INVALID_HANDLE_VALUE</b>, the calling process 
       must also specify a size for the file mapping object in the <i>dwMaximumSizeHigh</i> and 
       <i>dwMaximumSizeLow</i> parameters. In this scenario, 
       <b>CreateFileMapping</b> creates a file mapping object 
       of a specified size  that is backed by the system paging file instead of by a file in the file system.

### -param lpFileMappingAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> 
       structure that determines whether a returned handle can be inherited by child processes. The 
      <b>lpSecurityDescriptor</b> member of the 
      <b>SECURITY_ATTRIBUTES</b> structure specifies a 
      security descriptor for a new file mapping object.

If <i>lpAttributes</i> is <b>NULL</b>, the handle cannot be inherited 
      and the file mapping object gets a default security descriptor. The access control lists (ACL) in the default 
      security descriptor for a file mapping object come from the primary or impersonation token of the creator. For 
      more information, see 
      <a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File Mapping Security and Access Rights</a>.

### -param flProtect [in]

Specifies the page protection of the file mapping object. All mapped views of the object must be compatible 
       with this protection.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PAGE_EXECUTE_READ"></a><a id="page_execute_read"></a><dl>
<dt><b>PAGE_EXECUTE_READ</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
Allows views to be mapped for read-only, copy-on-write, or execute access.

The file handle specified by  the <i>hFile</i> parameter must be created with the 
         <b>GENERIC_READ</b> and <b>GENERIC_EXECUTE</b> access rights.

<b>Windows Server 2003 and Windows XP:  </b>This value is not available until Windows XP with SP2 and 
          Windows Server 2003 with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="PAGE_EXECUTE_READWRITE"></a><a id="page_execute_readwrite"></a><dl>
<dt><b>PAGE_EXECUTE_READWRITE</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
Allows views to be mapped for read-only, copy-on-write, read/write, or execute access.

The file   handle that the <i>hFile</i> parameter specifies must be created with the 
         <b>GENERIC_READ</b>, <b>GENERIC_WRITE</b>, and 
         <b>GENERIC_EXECUTE</b> access rights.

<b>Windows Server 2003 and Windows XP:  </b>This value is not available until Windows XP with SP2 and 
          Windows Server 2003 with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="PAGE_EXECUTE_WRITECOPY"></a><a id="page_execute_writecopy"></a><dl>
<dt><b>PAGE_EXECUTE_WRITECOPY</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
Allows views to be mapped for read-only, copy-on-write, or execute access. This value is equivalent to 
         <b>PAGE_EXECUTE_READ</b>.

The file handle that the <i>hFile</i> parameter specifies must be created with the 
         <b>GENERIC_READ</b> and <b>GENERIC_EXECUTE</b> access rights.

<b>Windows Vista:  </b>This value is not available until Windows Vista with SP1.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PAGE_READONLY"></a><a id="page_readonly"></a><dl>
<dt><b>PAGE_READONLY</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Allows views to be mapped for read-only or copy-on-write access. An attempt to write to a specific 
        region results in an access violation.

The file handle that  the <i>hFile</i> parameter 
        specifies must be created with the <b>GENERIC_READ</b> access right.

</td>
</tr>
<tr>
<td width="40%"><a id="PAGE_READWRITE"></a><a id="page_readwrite"></a><dl>
<dt><b>PAGE_READWRITE</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Allows views to be mapped for read-only, copy-on-write, or read/write access.

The file handle that the <i>hFile</i> parameter specifies must be created with the 
         <b>GENERIC_READ</b> and 
        <b>GENERIC_WRITE</b> access rights.

</td>
</tr>
<tr>
<td width="40%"><a id="PAGE_WRITECOPY"></a><a id="page_writecopy"></a><dl>
<dt><b>PAGE_WRITECOPY</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
Allows views to be mapped for read-only or copy-on-write access. This value is equivalent to 
         <b>PAGE_READONLY</b>.

The file handle that  the <i>hFile</i> parameter specifies must be created with the 
        <b>GENERIC_READ</b> access right.

</td>
</tr>
</table>
 

An application can specify one or more of the following attributes for the file mapping object by combining 
       them with one of the preceding page protection values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SEC_COMMIT"></a><a id="sec_commit"></a><dl>
<dt><b>SEC_COMMIT</b></dt>
<dt>0x8000000</dt>
</dl>
</td>
<td width="60%">
If the file mapping object is backed by the operating system paging file (the 
         <i>hfile</i> parameter is <b>INVALID_HANDLE_VALUE</b>), specifies that 
         when  a view of the file is mapped into a process address space, the entire range of pages is committed 
         rather than reserved. The system must have enough committable pages to hold the entire mapping. Otherwise, 
         <b>CreateFileMapping</b> fails.

This attribute has no effect for file mapping objects that are backed by executable image files or data 
         files (the <i>hfile</i> parameter is a handle to a file).

<b>SEC_COMMIT</b> cannot be combined with <b>SEC_RESERVE</b>.

If no attribute is specified, <b>SEC_COMMIT</b> is assumed. However, <b>SEC_COMMIT</b> must be explicitly specified when combining it with another <b>SEC_</b> attribute that requires it.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_IMAGE"></a><a id="sec_image"></a><dl>
<dt><b>SEC_IMAGE</b></dt>
<dt>0x1000000</dt>
</dl>
</td>
<td width="60%">
Specifies that the file that the  <i>hFile</i> parameter specifies is an executable 
         image file.

The <b>SEC_IMAGE</b> attribute must be combined with a page protection value such as 
         <b>PAGE_READONLY</b>. However, this page protection value has no effect on views of the 
         executable image file. Page protection for views of an executable image file is determined by the executable 
         file itself.

No other attributes are valid with <b>SEC_IMAGE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_IMAGE_NO_EXECUTE"></a><a id="sec_image_no_execute"></a><dl>
<dt><b>SEC_IMAGE_NO_EXECUTE</b></dt>
<dt>0x11000000</dt>
</dl>
</td>
<td width="60%">
Specifies that the file that the  <i>hFile</i> parameter specifies is an executable 
         image file that will not be executed and the loaded image file will have no forced integrity checks run. 
         Additionally, mapping a view of a file mapping object created with the 
         <b>SEC_IMAGE_NO_EXECUTE</b> attribute will not invoke driver callbacks registered using 
         the <a href="/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-pssetloadimagenotifyroutine">PsSetLoadImageNotifyRoutine</a> 
         kernel API.

The <b>SEC_IMAGE_NO_EXECUTE</b> attribute must be combined with the 
         <b>PAGE_READONLY</b> page protection value. No other attributes are valid with 
         <b>SEC_IMAGE_NO_EXECUTE</b>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows Server 2012 and Windows 8.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_LARGE_PAGES"></a><a id="sec_large_pages"></a><dl>
<dt><b>SEC_LARGE_PAGES</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Enables large pages to be used for file mapping objects that are backed by the operating system paging file 
         (the <i>hfile</i> parameter is <b>INVALID_HANDLE_VALUE</b>). This 
         attribute is not supported for file mapping objects that are backed by executable image files or data files 
         (the <i>hFile</i> parameter is a handle to an executable image or data file).

The maximum size of the file mapping object must be a multiple of the minimum size of a large page returned 
         by the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-getlargepageminimum">GetLargePageMinimum</a> function. If it is 
         not, <b>CreateFileMapping</b> fails. When mapping a 
         view of a file mapping object created with <b>SEC_LARGE_PAGES</b>, the base address and 
         view size must also be multiples of the minimum large page size.

<b>SEC_LARGE_PAGES</b> requires the 
         <a href="/windows/desktop/SecAuthZ/authorization-constants">SeLockMemoryPrivilege</a> 
         privilege to be enabled in the caller's token.

If <b>SEC_LARGE_PAGES</b> is specified, <b>SEC_COMMIT</b> must also 
         be specified.

<b>Windows Server 2003:  </b>This value is not supported until Windows Server 2003 with SP1.

<b>Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_NOCACHE"></a><a id="sec_nocache"></a><dl>
<dt><b>SEC_NOCACHE</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Sets all pages to be non-cacheable.

Applications should not use this attribute except when 
         explicitly required for a device. Using the interlocked functions with memory that is mapped with 
         <b>SEC_NOCACHE</b> can result in an 
         <b>EXCEPTION_ILLEGAL_INSTRUCTION</b> exception.

<b>SEC_NOCACHE</b> requires either the <b>SEC_RESERVE</b> or 
         <b>SEC_COMMIT</b> attribute to be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_RESERVE"></a><a id="sec_reserve"></a><dl>
<dt><b>SEC_RESERVE</b></dt>
<dt>0x4000000</dt>
</dl>
</td>
<td width="60%">
If the file mapping object is backed by the operating system paging file (the 
         <i>hfile</i> parameter is <b>INVALID_HANDLE_VALUE</b>), specifies that 
         when a view of the file is mapped into a process address space, the entire range of pages is reserved for 
         later use by the process rather than committed.

Reserved pages can be committed in subsequent calls to the 
         <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function. After the pages are 
         committed, they cannot be freed or decommitted with the 
         <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a> function.

This attribute has no effect for file mapping objects that are backed by executable image files or data 
         files (the <i>hfile</i> parameter is a handle to a file).

<b>SEC_RESERVE</b> cannot be combined with <b>SEC_COMMIT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SEC_WRITECOMBINE"></a><a id="sec_writecombine"></a><dl>
<dt><b>SEC_WRITECOMBINE</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Sets all pages to  be write-combined.

Applications should not use this attribute except when 
         explicitly required for a device. Using the interlocked functions with memory that is mapped with 
         <b>SEC_WRITECOMBINE</b> can result in an 
         <b>EXCEPTION_ILLEGAL_INSTRUCTION</b> exception.

<b>SEC_WRITECOMBINE</b> requires either the <b>SEC_RESERVE</b> or 
         <b>SEC_COMMIT</b> attribute to be set.

<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported until Windows Vista.

</td>
</tr>
</table>

### -param dwMaximumSizeHigh [in]

The high-order <b>DWORD</b> of the maximum size of the file mapping object.

### -param dwMaximumSizeLow [in]

The low-order <b>DWORD</b> of the maximum size of the file mapping object.

If this parameter and <i>dwMaximumSizeHigh</i> are 0 (zero), the maximum size of the file 
       mapping object is equal to the current size of the file that  <i>hFile</i> identifies.

An attempt to map a file with a length of 0 (zero) fails with an error code of 
       <b>ERROR_FILE_INVALID</b>. Applications should test for files with a length of 0 (zero) and 
       reject those files.

### -param lpName [in, optional]

The name of the file mapping object.

If this parameter matches the name of an existing mapping object, the function requests access to the 
       object with the protection that <i>flProtect</i> specifies.

If this parameter is <b>NULL</b>, the file mapping object is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, mutex, waitable timer, or 
       job object, the function fails, and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
       function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the 
       same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the 
       object in the global or session namespace. The remainder of the name can contain any character except the 
       backslash character (\\). Creating a file mapping object in the global namespace from a session other than 
       session zero requires the 
       <a href="/windows/desktop/SecAuthZ/authorization-constants">SeCreateGlobalPrivilege</a> 
       privilege. For more information, see 
       <a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.

Fast user switching is implemented by using Terminal Services sessions. The first user to log on uses session 
       0 (zero), the next user to log on uses session 1 (one), and so on. Kernel object names must follow the 
       guidelines that are outlined for Terminal Services so that applications can support multiple users.

## -returns

If the function succeeds, the return value is a handle to the newly created file mapping object.

If the object exists before the function call, the function returns a handle to the existing object (with its 
       current size, not the specified size), and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After a file mapping object is created, the size of the file must not exceed the size of the file mapping 
    object; if it does, not all of the file contents are available for sharing.

If an application specifies a size for the file mapping object that is larger than the size of the actual named 
    file on disk and if the page protection allows write access (that is, the <i>flProtect</i> 
    parameter specifies  <b>PAGE_READWRITE</b> or 
    <b>PAGE_EXECUTE_READWRITE</b>), then the file on disk is increased to match the specified size 
    of the file mapping object. If the file is extended, the contents of the file between the old end of the file and 
    the new end of the file are not guaranteed to be zero; the behavior is defined by the file system. If the file 
    on disk cannot be increased, <b>CreateFileMapping</b> fails 
    and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>  returns 
    <b>ERROR_DISK_FULL</b>.

The initial contents of the pages in a file mapping object backed by the operating system paging file are 0 
    (zero).

The handle that <b>CreateFileMapping</b> returns has 
    full access to a new file mapping object, and can be used with any function that requires a handle to a file 
    mapping object.

Multiple processes can share a view of the same file   by either using a single shared file mapping object or 
    creating separate file mapping objects backed by the same file. A single file mapping object can be shared by 
    multiple processes through inheriting the handle at process creation, duplicating the handle, or opening the file 
    mapping object by name. For more information, see the 
    <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>, 
    <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> and 
    <a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a> functions.

Creating a file mapping object does not actually map the view into a process address space. The 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> and 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a> functions map a view of a file into a 
    process address space.

With one important exception, file views derived from any file mapping object that is backed by the same file 
    are coherent or identical at a specific time. Coherency is guaranteed for views within a process and for views 
    that are mapped by different processes.

The exception is related to remote files. Although 
    <b>CreateFileMapping</b> works with remote files, it does 
    not keep them coherent. For example, if two computers both map a file as writable, and both change the same page, 
    each computer only sees its own writes to the page. When the data gets updated on the disk, it is not merged.

A mapped file and a file that is accessed by using the input and output (I/O) functions 
    (<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> and 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>) are not necessarily coherent.

Mapped views of a file mapping object maintain internal references to the object, and a file mapping object 
    does not close until all references to it are released. Therefore, to fully close a file mapping object, an 
    application must unmap all mapped views of the file mapping object by calling 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a> and  close the file mapping object 
    handle by calling <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>. These functions can be 
    called in any order.

When modifying a file through a mapped view, the last modification timestamp may not be updated automatically. 
    If required, the caller should use <a href="/windows/desktop/api/fileapi/nf-fileapi-setfiletime">SetFileTime</a> to set the 
    timestamp.

Creating a file mapping object in the global namespace from a session other than session zero requires the 
     <a href="/windows/desktop/SecAuthZ/authorization-constants">SeCreateGlobalPrivilege</a> privilege. 
     Note that this privilege check is limited to the creation of file mapping objects and does not apply to opening 
     existing ones. For example, if a service or the system creates a file mapping object in the global namespace, any 
     process running in any session can access that file mapping object provided that the caller has the required 
     access rights.

<b>Windows XP:  </b>The requirement described in the previous paragraph was introduced with Windows Server 2003 
      and Windows XP with SP2

Use structured exception handling to protect any code that writes to or reads from a file view. For more 
     information, see 
     <a href="/windows/desktop/Memory/reading-and-writing-from-a-file-view">Reading and Writing From a File View</a>.

To have a mapping with executable permissions, an application must call
     <b>CreateFileMapping</b> with either 
     <b>PAGE_EXECUTE_READWRITE</b> or <b>PAGE_EXECUTE_READ</b>, and then 
     call <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> with 
     <code>FILE_MAP_EXECUTE | FILE_MAP_WRITE</code> or 
     <code>FILE_MAP_EXECUTE | FILE_MAP_READ</code>.

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
 


#### Examples

For an example, see 
     <a href="/windows/desktop/Memory/creating-named-shared-memory">Creating Named Shared Memory</a> or 
     <a href="/windows/desktop/Memory/creating-a-file-mapping-using-large-pages">Creating a File Mapping Using Large Pages</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappingnumaa">CreateFileMappingNuma</a>



<a href="/windows/desktop/Memory/creating-a-file-mapping-object">Creating a File Mapping Object</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>



File Mapping Functions



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a>



<a href="/windows/desktop/Memory/memory-management-functions">Memory Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>
