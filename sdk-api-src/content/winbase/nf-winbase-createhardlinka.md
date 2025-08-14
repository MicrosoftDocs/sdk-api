---
UID: NF:winbase.CreateHardLinkA
title: CreateHardLinkA function (winbase.h)
description: Establishes a hard link between an existing file and a new file. (ANSI)
helpviewer_keywords: ["CreateHardLinkA", "winbase/CreateHardLinkA"]
old-location: fs\createhardlink.htm
tech.root: fs
ms.assetid: 9b0d3f04-775f-44ea-b563-93dee29a278a
ms.date: 12/05/2018
ms.keywords: CreateHardLink, CreateHardLink function [Files], CreateHardLinkA, CreateHardLinkW, _win32_createhardlink, base.createhardlink, fs.createhardlink, winbase/CreateHardLink, winbase/CreateHardLinkA, winbase/CreateHardLinkW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateHardLinkW (Unicode) and CreateHardLinkA (ANSI)
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
 - CreateHardLinkA
 - winbase/CreateHardLinkA
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
api_name:
 - CreateHardLink
 - CreateHardLinkA
 - CreateHardLinkW
---

# CreateHardLinkA function


## -description

Establishes a hard link between an existing file and a new file. This function is only 
    supported on the NTFS file system, and only for files, not directories.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-createhardlinktransacteda">CreateHardLinkTransacted</a> function.

## -parameters

### -param lpFileName [in]

The name of the new file.
      

This parameter may include the path but cannot specify the name of a directory.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.



### -param lpExistingFileName [in]

The name of the existing file.
      

This parameter may include the path cannot specify the name of a directory.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpSecurityAttributes

Reserved; must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The maximum number of hard links that can be created with this function is 1023 per file. If more than 1023 links are created for a file, an error results.

If you pass a name longer than MAX_PATH characters to the *lpFileName* or *lpExistingFileName* parameter of the ANSI version of this function or to the Unicode version of this function without prepending "\\\\?\\" to the path, the function returns ERROR_PATH_NOT_FOUND.

## -remarks

Any directory entry for a file that is created with 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> or 
    <b>CreateHardLink</b> is a hard link to an associated file. 
    An additional hard link that is created with the 
    <b>CreateHardLink</b> 
    function allows you to have multiple directory entries for a file, that is, multiple hard links to the same file, 
    which can be different names in the same directory, or the same or different names in different directories. 
    However, all hard links to a file must be on the same volume.

Because hard links are only directory entries for a file, many changes to that file are instantly visible to 
    applications that access it through the hard links that reference it. However, the directory entry size and 
    attribute information is updated only for the link through which the change was made.

The security descriptor belongs to the file to which a hard link points. The link itself is only a directory 
    entry, and does not have a security descriptor. Therefore, when you change the security descriptor of a hard link, 
    you a change the security descriptor of the underlying file, and all hard links that point to the file allow the 
    newly specified access. You cannot give a file different security descriptors on a per-hard-link basis.

This function does not modify the security descriptor of the file to be linked to, even if security descriptor 
    information is passed in the <i>lpSecurityAttributes</i> parameter.

Use <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a> to delete hard links. You can delete 
    them in any order regardless of the order in which they are created.

Flags, attributes, access, and sharing that are specified in 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> operate on a per-file basis. That is, if you 
    open a file that does not allow sharing, another application cannot share the file by creating a new hard link to 
    the file.

When you create a hard link on the NTFS file system, the file attribute information in the directory entry is 
    refreshed only when the file is opened, or when 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a> is called with 
    the handle of a specific file.

Symbolic link behavior—If the path points to a symbolic link, the function creates a hard 
     link to the symbolic link.

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
Yes

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
 

Note that SMB 3.0 does not support creation of hard links on shares with continuous availability capability.


#### Examples

The following code snippet shows you how to call 
    <b>CreateHardLink</b> so that it does not modify the security 
    descriptor of a file. The <i>pszExistingFileName</i> parameter can be the original file name, 
    or any existing link to a file. After this code is executed, <i>pszNewLinkName</i> refers to 
    the file.


```cpp
  BOOL fCreatedLink = CreateHardLink( pszNewLinkName, 
                                      pszExistingFileName, 
                                      NULL ); // reserved, must be NULL

  if ( fCreatedLink == FALSE )
   {
    ;// handle error condition
   }

```






> [!NOTE]
> The winbase.h header defines CreateHardLink as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createhardlinktransacteda">CreateHardLinkTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/hard-links-and-junctions">Hard Links and Junctions</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
