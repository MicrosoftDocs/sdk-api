---
UID: NF:memoryapi.CreateFileMapping2
title: CreateFileMapping2
description: Creates or opens a named or unnamed file mapping object for a specified file. You can specify a preferred NUMA node for the physical memory as an extended parameter; see the *ExtendedParameters* parameter.
ms.date: 10/22/2020
tech.root: base
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: memoryapi.h
req.idl: 
req.include-header: Windows.h, Memoryapi.h
req.irql: 
req.kmdf-ver: 
req.lib: onecore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - Kernel32.dll
api_name:
 - CreateFileMapping2
f1_keywords:
 - CreateFileMapping2
 - memoryapi/CreateFileMapping2
dev_langs:
 - c++
---

# CreateFileMapping2 function

## -description

Creates or opens a named or unnamed file mapping object for a specified file. You can specify a preferred NUMA node for the physical memory as an extended parameter; see the *ExtendedParameters* parameter.

## -parameters

### -param File

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to the file from which to create a file mapping object.

The file must be opened with access rights that are compatible with the protection flags that the <i>flProtect</i> parameter specifies. It is not required, but it is recommended that files you intend to map be opened for exclusive access. For more information, see <a href="/windows/win32/FileIO/file-security-and-access-rights">File security and access rights</a>.

If <i>hFile</i> is <b>INVALID_HANDLE_VALUE</b>, the calling process must also specify a size for the file mapping object in the <i>dwMaximumSizeHigh</i> and <i>dwMaximumSizeLow</i> parameters. In this scenario, <b>CreateFileMapping</b> creates a file mapping object of a specified size  that is backed by the system paging file instead of by a file in the file system.

### -param SecurityAttributes

Type: \_In_opt\_ **[SECURITY_ATTRIBUTES](/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes)\***

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that determines whether a returned handle can be inherited by child processes. The <b>lpSecurityDescriptor</b> member of the <b>SECURITY_ATTRIBUTES</b> structure specifies a security descriptor for a new file mapping object.

If <i>lpAttributes</i> is <b>NULL</b>, the handle cannot be inherited and the file mapping object gets a default security descriptor. The access control lists (ACL) in the default security descriptor for a file mapping object come from the primary or impersonation token of the creator. For more information, see <a href="/windows/win32/Memory/file-mapping-security-and-access-rights">File Mapping Security and Access Rights</a>.

### -param DesiredAccess

Type: \_In\_ **[ULONG](/windows/win32/winprog/windows-data-types)**

The desired access mask for the returned file mapping handle. For a list of access rights, see [File-mapping security and access rights](/windows/win32/memory/file-mapping-security-and-access-rights).

### -param PageProtection

Type: \_In\_ **[ULONG](/windows/win32/winprog/windows-data-types)**

Specifies the page protection of the file mapping object. All mapped views of the object must be compatible with this protection.

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

### -param AllocationAttributes

Type: \_In\_ **[ULONG](/windows/win32/winprog/windows-data-types)**

You can specify one or more of the following attributes for the file mapping object. Also see the *PageProtection* parameter.

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

If no attribute is specified, <b>SEC_COMMIT</b> is assumed.

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
         by the <a href="/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum">GetLargePageMinimum</a> function. If it is 
         not, <b>CreateFileMapping</b> fails. When mapping a 
         view of a file mapping object created with <b>SEC_LARGE_PAGES</b>, the base address and 
         view size must also be multiples of the minimum large page size.

<b>SEC_LARGE_PAGES</b> requires the 
         <a href="/windows/win32/SecAuthZ/authorization-constants">SeLockMemoryPrivilege</a> 
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
         <a href="/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function. After the pages are 
         committed, they cannot be freed or decommitted with the 
         <a href="/windows/win32/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a> function.

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

### -param MaximumSize

Type: \_In\_ **[ULONG64](/windows/win32/winprog/windows-data-types)**

The maximum size of the file mapping object.

If this parameter is 0 (zero), then the maximum size of the file mapping object is equal to the current size of the file that <i>hFile</i> identifies.

An attempt to map a file with a length of 0 (zero) fails with an error code of <b>ERROR_FILE_INVALID</b>. You should test for files with a length of 0 (zero), and reject those files.

### -param Name

Type: \_In_opt\_ **[PCWSTR](/windows/win32/winprog/windows-data-types)**

The name of the file mapping object.

If this parameter matches the name of an existing mapping object, then the function requests access to the object with the protection that <i>flProtect</i> specifies.

If this parameter is <b>NULL</b>, then the file mapping object is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, mutex, waitable timer, or job object, the function fails, and the <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). Creating a file mapping object in the global namespace from a session other than session zero requires the <a href="/windows/win32/SecAuthZ/authorization-constants">SeCreateGlobalPrivilege</a> privilege. For more information, see <a href="/windows/win32/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.

Fast user switching is implemented by using Terminal Services sessions. The first user to log on uses session 0 (zero), the next user to log on uses session 1 (one), and so on. Kernel object names must follow the guidelines that are outlined for Terminal Services so that applications can support multiple users.

### -param ExtendedParameters

Type: \_Inout\_updates\_opt\_(ParameterCount) **[MEM_EXTENDED_PARAMETER](/windows/win32/api/winnt/ns-winnt-mem_extended_parameter)\***

An optional pointer to one or more extended parameters of type <a href="/windows/win32/api/winnt/ns-winnt-mem_extended_parameter">MEM_EXTENDED_PARAMETER</a>. Each of those extended parameter values can itself have a <i>Type</i> field of either <b>MemExtendedParameterAddressRequirements</b> or <b>MemExtendedParameterNumaNode</b>. If no <b>MemExtendedParameterNumaNode</b> extended parameter is provided, then the behavior is the same as for the <a href="/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>/<a href="/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> functions (that is, the preferred NUMA node for the physical pages is determined based on the ideal processor of the thread that first accesses the memory).

### -param ParameterCount

_In_ ULONG ParameterCount

The number of extended parameters pointed to by *ExtendedParameters*.

## -returns

If the function succeeds, the return value is a handle to the newly created file mapping object.

If the object exists before the function call, the function returns a handle to the existing object (with its current size, not the specified size), and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

See the **Remarks** for [CreateFileMapping](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw#remarks).

## Examples

For an example, see <a href="/windows/win32/memory/creating-named-shared-memory">Creating named shared memory</a>, or <a href="/windows/win32/Memory/creating-a-file-mapping-using-large-pages">Creating a file mapping using large pages</a>.

## -see-also

<a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>

<a href="/windows/win32/api/winbase/nf-winbase-createfilemappingnumaa">CreateFileMappingNuma</a>

<a href="/windows/win32/Memory/creating-a-file-mapping-object">Creating a file mapping object</a>

<a href="/windows/win32/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>

<a href="/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a>

<a href="/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex">MapViewOfFileEx</a>

<a href="/windows/win32/Memory/memory-management-functions">Memory management functions</a>

<a href="/windows/win32/api/winbase/nf-winbase-openfilemappinga">OpenFileMapping</a>

<a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a>

<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>

<a href="/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a>

<a href="/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>

<a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a>
