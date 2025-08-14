---
UID: NF:winbase.CreateDirectoryExW
title: CreateDirectoryExW function (winbase.h)
description: Creates a new directory with the attributes of a specified template directory. (Unicode)
helpviewer_keywords: ["CreateDirectoryEx", "CreateDirectoryEx function [Files]", "CreateDirectoryExW", "_win32_createdirectoryex", "base.createdirectoryex", "fs.createdirectoryex", "winbase/CreateDirectoryEx", "winbase/CreateDirectoryExW"]
old-location: fs\createdirectoryex.htm
tech.root: fs
ms.assetid: 287996f8-e8ca-4b72-a5f6-016754785c5c
ms.date: 12/05/2018
ms.keywords: CreateDirectoryEx, CreateDirectoryEx function [Files], CreateDirectoryExA, CreateDirectoryExW, _win32_createdirectoryex, base.createdirectoryex, fs.createdirectoryex, winbase/CreateDirectoryEx, winbase/CreateDirectoryExA, winbase/CreateDirectoryExW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateDirectoryExW (Unicode) and CreateDirectoryExA (ANSI)
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
 - CreateDirectoryExW
 - winbase/CreateDirectoryExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l2-1-4.dll
 - api-ms-win-core-file-l2-1-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-1.dll
 - API-MS-Win-Core-File-l2-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - API-Ms-Win-Core-File-Ansi-L2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - CreateDirectoryEx
 - CreateDirectoryExA
 - CreateDirectoryExW
---

# CreateDirectoryExW function


## -description

Creates a new directory with the attributes of a specified template directory. If the 
    underlying file system supports security on files and directories, the function applies a specified security 
    descriptor to the new directory. The new directory retains the other attributes of the specified template 
    directory.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-createdirectorytransacteda">CreateDirectoryTransacted</a> function.

## -parameters

### -param lpTemplateDirectory [in]

The path of the directory to use as a template when creating the new directory.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpNewDirectory [in]

The path of the directory to be created.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpSecurityAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> 
       structure. The <b>lpSecurityDescriptor</b> member of the structure specifies a security 
       descriptor for the new directory.

If <i>lpSecurityAttributes</i> is <b>NULL</b>, the directory gets a 
       default security descriptor. The access control lists (ACL) in the default security descriptor for a directory 
       are inherited from its parent directory.

The target file system must support security on files and directories for this parameter to have an effect. 
       This is indicated when <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a> 
       returns <b>FS_PERSISTENT_ACLS</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
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
One or more intermediate directories do not exist. This function only creates the final directory in the 
        path. To create all intermediate directories on the path, use the 
        <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedirectoryexa">SHCreateDirectoryEx</a> function.

</td>
</tr>
</table>

## -remarks

The <b>CreateDirectoryEx</b> function allows you to 
    create directories that inherit stream information from other directories. This function is useful, for example, 
    when you are using Macintosh directories, which have a resource stream that is needed to properly identify 
    directory contents as an attribute.

Some file systems, such as the NTFS file system, support compression or encryption for individual files and 
    directories. On volumes formatted for such a file system, a new directory inherits the compression and encryption 
    attributes of its parent directory.

You can obtain a handle to a directory by calling the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function with the 
    <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag set. For a code example, see 
    <b>CreateFile</b>.

To support inheritance functions that query the security descriptor of this 
     object can heuristically determine and report that inheritance is in effect. For more information, see 
     <a href="/windows/desktop/SecAuthZ/automatic-propagation-of-inheritable-aces">Automatic Propagation of Inheritable ACEs</a>.

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
 





> [!NOTE]
> The winbase.h header defines CreateDirectoryEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createdirectorytransacteda">CreateDirectoryTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/creating-and-deleting-directories">Creating and Deleting Directories</a>



<a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-removedirectorya">RemoveDirectory</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>
