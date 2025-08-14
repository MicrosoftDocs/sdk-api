---
UID: NF:memoryapi.CreateFileMappingFromApp
title: CreateFileMappingFromApp function (memoryapi.h)
description: Creates or opens a named or unnamed file mapping object for a specified file from a Windows Store app.
helpviewer_keywords: ["CreateFileMappingFromApp","CreateFileMappingFromApp function","PAGE_READONLY","PAGE_READWRITE","PAGE_WRITECOPY","SEC_COMMIT","SEC_IMAGE_NO_EXECUTE","SEC_LARGE_PAGES","SEC_NOCACHE","SEC_RESERVE","SEC_WRITECOMBINE","base.createfilemappingfromapp","memoryapi/CreateFileMappingFromApp"]
old-location: base\createfilemappingfromapp.htm
tech.root: base
ms.assetid: ef7ad1aa-2ce7-4a77-a57e-d6e55d58b8d3
ms.date: 12/05/2018
ms.keywords: CreateFileMappingFromApp, CreateFileMappingFromApp function, PAGE_READONLY, PAGE_READWRITE, PAGE_WRITECOPY, SEC_COMMIT, SEC_IMAGE_NO_EXECUTE, SEC_LARGE_PAGES, SEC_NOCACHE, SEC_RESERVE, SEC_WRITECOMBINE, base.createfilemappingfromapp, memoryapi/CreateFileMappingFromApp
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
 - CreateFileMappingFromApp
 - memoryapi/CreateFileMappingFromApp
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
 - CreateFileMappingFromApp
---

# CreateFileMappingFromApp function


## -description

Creates or opens a named or unnamed file mapping object for a specified file from a 
    Windows Store app.

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
       <b>CreateFileMappingFromApp</b> creates a file 
       mapping object of a specified size  that is backed by the system paging file instead of by a file in the file 
       system.

### -param SecurityAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> 
       structure that determines whether a returned handle can be inherited by child processes. The 
       <b>lpSecurityDescriptor</b> member of the 
       <b>SECURITY_ATTRIBUTES</b> structure specifies a 
       security descriptor for a new file mapping object.

If <i>SecurityAttributes</i> is <b>NULL</b>, the handle cannot be 
       inherited and the file mapping object gets a default security descriptor. The access control lists (ACL) in the 
       default security descriptor for a file mapping object come from the primary or impersonation token of the 
       creator. For more information, see 
       <a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">File Mapping Security and Access Rights</a>.

### -param PageProtection [in]

Specifies the page protection of the file mapping object. All mapped views of the object must be compatible 
       with this protection.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
         <b>GENERIC_READ</b> and <b>GENERIC_WRITE</b> access rights.

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
         <b>CreateFileMappingFromApp</b> fails.

This attribute has no effect for file mapping objects that are backed by executable image files or data 
         files (the <i>hfile</i> parameter is a handle to a file).

<b>SEC_COMMIT</b> cannot be combined with <b>SEC_RESERVE</b>.

If no attribute is specified, <b>SEC_COMMIT</b> is assumed.

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
         not, <b>CreateFileMappingFromApp</b> fails. 
         When mapping a view of a file mapping object created with <b>SEC_LARGE_PAGES</b>, the base 
         address and view size must also be multiples of the minimum large page size.

<b>SEC_LARGE_PAGES</b> requires the 
         <a href="/windows/desktop/SecAuthZ/authorization-constants">SeLockMemoryPrivilege</a> 
         privilege to be enabled in the caller's token.

If <b>SEC_LARGE_PAGES</b> is specified, <b>SEC_COMMIT</b> must also 
         be specified.

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

</td>
</tr>
</table>

### -param MaximumSize [in]

The maximum size of the file mapping object.

An attempt to map a file with a length of 0 (zero) fails with an error code of 
       <b>ERROR_FILE_INVALID</b>. Applications should test for files with a length of 0 (zero) and 
       reject those files.

### -param Name [in, optional]

The name of the file mapping object.

If this parameter matches the name of an existing mapping object, the function requests access to the 
       object with the protection that <i>flProtect</i> specifies.

If this parameter is <b>NULL</b>, the file mapping object is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, mutex, waitable timer, 
       or job object, the function fails, and the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns 
       <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session 
       namespace. The remainder of the name can contain any character except the backslash character (\\). Creating a 
       file mapping object in the global namespace from a session other than session zero requires the 
       <a href="/windows/desktop/SecAuthZ/authorization-constants">SeCreateGlobalPrivilege</a> 
       privilege. For more information, see 
       <a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.

Fast user switching is implemented by using Terminal Services sessions. The first user to log on uses session 
       0 (zero), the next user to log on uses session 1 (one), and so on. Kernel object names must follow the 
       guidelines that are outlined for Terminal Services so that applications can support multiple users.

## -returns

If the function succeeds, the return value is a handle to the newly created file mapping object.

If the object exists before the function call, the function returns a handle to the existing object (with its 
       current size, not the specified size), and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> 
       returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, 
       call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After a file mapping object is created, the size of the file must not exceed the size of the file mapping 
    object; if it does, not all of the file contents are available for sharing.

If an application specifies a size for the file mapping object that is larger than the size of the actual 
    named file on disk and if the page protection allows write access (that is, the 
    <i>flProtect</i> parameter specifies  <b>PAGE_READWRITE</b>), then the file 
    on disk is increased to match the specified size of the file mapping object. If the file is extended, the contents 
    of the file between the old end of the file and the new end of the file are not guaranteed to be zero; the 
    behavior is defined by the file system. If the file on disk cannot be increased, 
    <b>CreateFileMappingFromApp</b> fails and 
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>  returns 
    <b>ERROR_DISK_FULL</b>.

The initial contents of the pages in a file mapping object backed by the operating system paging file are 0 
    (zero).

The handle that <b>CreateFileMappingFromApp</b> 
    returns has full access to a new file mapping object, and can be used with any function that requires a handle to 
    a file mapping object.

Multiple processes can share a view of the same file   by either using a single shared file mapping object or 
    creating separate file mapping objects backed by the same file. A single file mapping object can be shared by 
    multiple processes through inheriting the handle at process creation, duplicating the handle, or opening the file 
    mapping object by name. For more information, see the 
    <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>, 
    <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> and 
    <a href="/windows/desktop/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a> functions.

Creating a file mapping object does not actually map the view into a process address space. The 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a> function map a view of a file into a 
    process address space.

With one important exception, file views derived from any file mapping object that is backed by the same file 
    are coherent or identical at a specific time. Coherency is guaranteed for views within a process and for views 
    that are mapped by different processes.

The exception is related to remote files. Although 
    <b>CreateFileMappingFromApp</b> works with remote 
    files, it does not keep them coherent. For example, if two computers both map a file as writable, and both change 
    the same page, each computer only sees its own writes to the page. When the data gets updated on the disk, it is 
    not merged.

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

Use structured exception handling to protect any code that writes to or reads from a file view. For more 
    information, see 
    <a href="/windows/desktop/Memory/reading-and-writing-from-a-file-view">Reading and Writing From a File View</a>.

 You can only successfully request executable protection if your app has the <b>codeGeneration</b> capability.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>



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