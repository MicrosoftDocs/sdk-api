---
UID: NF:fileapi.CreateDirectoryW
title: CreateDirectoryW function (fileapi.h)
description: Creates a new directory. (CreateDirectoryW)
helpviewer_keywords: ["CreateDirectory", "CreateDirectory function [Files]", "CreateDirectoryW", "_win32_createdirectory", "base.createdirectory", "fileapi/CreateDirectory", "fileapi/CreateDirectoryW", "fs.createdirectory"]
old-location: fs\createdirectory.htm
tech.root: fs
ms.assetid: f8ca8b10-c8bd-4285-8a40-dbec4c24729c
ms.date: 12/05/2018
ms.keywords: CreateDirectory, CreateDirectory function [Files], CreateDirectoryA, CreateDirectoryW, _win32_createdirectory, base.createdirectory, fileapi/CreateDirectory, fileapi/CreateDirectoryA, fileapi/CreateDirectoryW, fs.createdirectory, winbase/CreateDirectory, winbase/CreateDirectoryA, winbase/CreateDirectoryW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateDirectoryW (Unicode) and CreateDirectoryA (ANSI)
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
 - CreateDirectoryW
 - fileapi/CreateDirectoryW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - CreateDirectory
 - CreateDirectoryA
 - CreateDirectoryW
---

# CreateDirectoryW function


## -description

Creates a new directory. If the underlying file system supports security on files and 
    directories, the function applies a specified security descriptor to the new directory.

To specify a template directory, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a> function.

To perform this 
    operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-createdirectorytransacteda">CreateDirectoryTransacted</a> function.

## -parameters

### -param lpPathName [in]

The path of the directory to be created.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpSecurityAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> 
       structure. The <b>lpSecurityDescriptor</b> member of the structure specifies a security 
       descriptor for the new directory. If <i>lpSecurityAttributes</i> is 
       <b>NULL</b>, the directory gets a default security descriptor. The ACLs in the default 
       security descriptor for a  directory are inherited from its parent directory.

The target file system must support security on files and directories for this parameter to have an effect. 
       (This is indicated when <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a> 
       returns <b>FS_PERSISTENT_ACLS</b>.)

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible errors include the 
       following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified directory already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
One or more intermediate directories do not exist; this function will only create the final directory in 
        the path.

</td>
</tr>
</table>

## -remarks

Some file systems, such as the NTFS file system, support compression or encryption for individual files and 
    directories. On volumes formatted for such a file system, a new directory inherits the compression and encryption 
    attributes of its parent directory. 

An application can obtain a handle to a directory by calling 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
    <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag set. For a code example, see 
    <b>CreateFile</b>.

To support inheritance functions that query the security descriptor of this object may heuristically determine 
    and report that inheritance is in effect. See 
    <a href="/windows/desktop/SecAuthZ/automatic-propagation-of-inheritable-aces">Automatic Propagation of Inheritable ACEs</a> 
    for more information.

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
     <a href="/windows/desktop/FileIO/retrieving-and-changing-file-attributes">Retrieving and Changing File Attributes</a>.

<div class="code"></div>




> [!NOTE]
> The fileapi.h header defines CreateDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createdirectoryexa">CreateDirectoryEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createdirectorytransacteda">CreateDirectoryTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/creating-and-deleting-directories">Creating and Deleting Directories</a>



<a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-removedirectorya">RemoveDirectory</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>
