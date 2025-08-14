---
UID: NF:winbase.CreateHardLinkTransactedW
title: CreateHardLinkTransactedW function (winbase.h)
description: Establishes a hard link between an existing file and a new file as a transacted operation. (Unicode)
helpviewer_keywords: ["CreateHardLinkTransacted", "CreateHardLinkTransacted function [Files]", "CreateHardLinkTransactedW", "fs.createhardlinktransacted", "winbase/CreateHardLinkTransacted", "winbase/CreateHardLinkTransactedW"]
old-location: fs\createhardlinktransacted.htm
tech.root: fs
ms.assetid: 27dd5b0a-08ef-4757-8f51-03d9918028c8
ms.date: 12/05/2018
ms.keywords: CreateHardLinkTransacted, CreateHardLinkTransacted function [Files], CreateHardLinkTransactedA, CreateHardLinkTransactedW, fs.createhardlinktransacted, winbase/CreateHardLinkTransacted, winbase/CreateHardLinkTransactedA, winbase/CreateHardLinkTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateHardLinkTransactedW (Unicode) and CreateHardLinkTransactedA (ANSI)
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
 - CreateHardLinkTransactedW
 - winbase/CreateHardLinkTransactedW
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
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - CreateHardLinkTransacted
 - CreateHardLinkTransactedA
 - CreateHardLinkTransactedW
---

# CreateHardLinkTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Establishes a hard link between an existing file and a new file as a transacted operation. 
    This function is only supported on the NTFS file system, and only for files, not directories.

## -parameters

### -param lpFileName [in]

The name of the new file.

This parameter cannot specify the name of a directory.

### -param lpExistingFileName [in]

The name of the existing file.

This parameter cannot specify the name of a directory.

### -param lpSecurityAttributes

Reserved; must be <b>NULL</b>.

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The maximum number of hard links that can be created with this function is 1023 per file. If more than 1023 
       links are created for a file, an error results.

The files must reside on the local computer; otherwise, 
       the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

## -remarks

Any directory entry for a file that is created with 
    <a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a> or 
    <b>CreateHardLinkTransacted</b> is a hard link to an 
    associated file. An additional hard link that is created with the 
    <b>CreateHardLinkTransacted</b> function allows you to 
    have multiple directory entries for a file, that is, multiple hard links to the same file, which can be different 
    names in the same directory, or the same or different names in different directories. However, all hard links to a 
    file must be on the same volume.

Because hard links are only directory entries for a file, when an application modifies a file through any hard 
    link, all applications that use any other hard link to the file see the changes. Also, all of the directory 
    entries are updated if the file changes. For example, if a file size changes, all of the hard links to the file 
    show the new file size.

The security descriptor belongs to the file to which a hard link points. The link itself is only a directory 
    entry, and does not have a security descriptor. Therefore, when you change the security descriptor of a hard link, 
    you a change the security descriptor of the underlying file, and all hard links that point to the file allow the 
    newly specified access. You cannot give a file different security descriptors on a per-hard-link basis.

This function does not modify the security descriptor of the file to be linked to, even if security descriptor 
    information is passed in the <i>lpSecurityAttributes</i> parameter.

Use <a href="/windows/desktop/api/winbase/nf-winbase-deletefiletransacteda">DeleteFileTransacted</a> to delete hard links. 
    You can delete them in any order regardless of the order in which they are created.

Flags, attributes, access, and sharing that are specified in 
    <a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a> operate on a per-file basis. 
    That is, if you open a file that does not allow sharing, another application cannot share the file by creating a 
    new hard link to the file.

When you create a hard link on the NTFS file system, the file attribute information in the directory entry is 
    refreshed only when the file is opened, or when 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a> is called with the 
    handle of a specific file.

<b>Symbolic links:  </b>If the path points to a symbolic link, the function creates a hard link to the target.

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
 

Note that SMB 3.0 does not support TxF.





> [!NOTE]
> The winbase.h header defines CreateHardLinkTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deletefiletransacteda">DeleteFileTransacted</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/hard-links-and-junctions">Hard Links and Junctions</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
