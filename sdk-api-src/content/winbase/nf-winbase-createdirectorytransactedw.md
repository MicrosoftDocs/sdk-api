---
UID: NF:winbase.CreateDirectoryTransactedW
title: CreateDirectoryTransactedW function (winbase.h)
description: Creates a new directory as a transacted operation, with the attributes of a specified template directory. (Unicode)
helpviewer_keywords: ["CreateDirectoryTransacted", "CreateDirectoryTransacted function [Files]", "CreateDirectoryTransactedW", "fs.createdirectorytransacted", "winbase/CreateDirectoryTransacted", "winbase/CreateDirectoryTransactedW"]
old-location: fs\createdirectorytransacted.htm
tech.root: fs
ms.assetid: 75663b30-5bd9-4de7-8e4f-dc58016c2c40
ms.date: 12/05/2018
ms.keywords: CreateDirectoryTransacted, CreateDirectoryTransacted function [Files], CreateDirectoryTransactedA, CreateDirectoryTransactedW, fs.createdirectorytransacted, winbase/CreateDirectoryTransacted, winbase/CreateDirectoryTransactedA, winbase/CreateDirectoryTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateDirectoryTransactedW (Unicode) and CreateDirectoryTransactedA (ANSI)
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
 - CreateDirectoryTransactedW
 - winbase/CreateDirectoryTransactedW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - Ext-MS-Win-Kernel32-Transacted-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - CreateDirectoryTransacted
 - CreateDirectoryTransactedA
 - CreateDirectoryTransactedW
---

# CreateDirectoryTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Creates a new directory as a transacted operation, with the attributes of a specified template 
    directory. If the underlying file system supports security on files and directories, the function 
    applies a specified security descriptor to the new directory. The new directory retains the other attributes of 
    the specified template directory.

## -parameters

### -param lpTemplateDirectory [in, optional]

The path of the directory to use as a template when creating the new directory.  This parameter can be 
       <b>NULL</b>..

The directory must reside on the local computer; otherwise, the function fails and the last error code is set 
       to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpNewDirectory [in]

The path of the directory to be created.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details..

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

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

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
<dt><b>ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION</b></dt>
</dl>
</td>
<td width="60%">
You cannot create a child directory with a parent directory that has encryption disabled.

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
        path.

</td>
</tr>
</table>

## -remarks

The <b>CreateDirectoryTransacted</b> function 
    allows you to create directories that inherit stream information from other directories. This function is useful, 
    for example, when you are using Macintosh directories, which have a resource stream that is needed to properly 
    identify directory contents as an attribute.

Some file systems, such as the NTFS file system, support compression or encryption for individual files and 
    directories. On volumes formatted for such a file system, a new directory inherits the compression and encryption 
    attributes of its parent directory.

This function fails with <b>ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION</b> if you try to create a 
    child directory with a parent directory that has encryption disabled.

You can obtain a handle to a directory by calling the 
    <a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a> function with the 
     <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag set.

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
No

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
 

SMB 3.0 does not support TxF.





> [!NOTE]
> The winbase.h header defines CreateDirectoryTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>



<a href="/windows/desktop/FileIO/creating-and-deleting-directories">Creating and Deleting Directories</a>



<a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-removedirectorytransacteda">RemoveDirectoryTransacted</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
