---
UID: NF:winbase.CreateHardLinkA
title: CreateHardLinkA function
author: windows-sdk-content
description: Establishes a hard link between an existing file and a new file.
old-location: fs\createhardlink.htm
tech.root: fileio
ms.assetid: 9b0d3f04-775f-44ea-b563-93dee29a278a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateHardLink, CreateHardLink function [Files], CreateHardLinkA, CreateHardLinkW, _win32_createhardlink, base.createhardlink, fs.createhardlink, winbase/CreateHardLink, winbase/CreateHardLinkA, winbase/CreateHardLinkW
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateHardLinkA function


## -description


Establishes a hard link between an existing file and a new file. This function is only 
    supported on the NTFS file system, and only for files, not directories.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/27dd5b0a-08ef-4757-8f51-03d9918028c8">CreateHardLinkTransacted</a> function.


## -parameters




### -param lpFileName [in]

The name of the new file.
      

This parameter may include the path but cannot specify the name of a directory.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CreateHardLinkW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpExistingFileName [in]

The name of the existing file.
      

This parameter may include the path cannot specify the name of a directory.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CopyFileW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpSecurityAttributes

Reserved; must be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The maximum number of hard links that can be created with this function is 1023 per file. If more than 1023 
       links are created for a file, an error results.




## -remarks



Any directory entry for a file that is created with 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> or 
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

Use <a href="https://msdn.microsoft.com/0b947a85-816b-4374-a8f8-c369e366a17d">DeleteFile</a> to delete hard links. You can delete 
    them in any order regardless of the order in which they are created.

Flags, attributes, access, and sharing that are specified in 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> operate on a per-file basis. That is, if you 
    open a file that does not allow sharing, another application cannot share the file by creating a new hard link to 
    the file.

When you create a hard link on the NTFS file system, the file attribute information in the directory entry is 
    refreshed only when the file is opened, or when 
    <a href="https://msdn.microsoft.com/d026ee3a-c165-42a2-a4e1-efccdafbefc5">GetFileInformationByHandle</a> is called with 
    the handle of a specific file.

Symbolic link behavior—If the path points to a symbolic link, the function creates a hard 
     link to the target.

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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>  BOOL fCreatedLink = CreateHardLink( pszNewLinkName, 
                                      pszExistingFileName, 
                                      NULL ); // reserved, must be NULL

  if ( fCreatedLink == FALSE )
   {
    ;// handle error condition
   }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/27dd5b0a-08ef-4757-8f51-03d9918028c8">CreateHardLinkTransacted</a>



<a href="https://msdn.microsoft.com/0b947a85-816b-4374-a8f8-c369e366a17d">DeleteFile</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/f9e40a86-a4a6-4524-8045-312da72dc655">Hard Links and Junctions</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>
 

 

