---
UID: NF:winbase.CreateDirectoryExW
title: CreateDirectoryExW function
author: windows-sdk-content
description: Creates a new directory with the attributes of a specified template directory.
old-location: fs\createdirectoryex.htm
old-project: FileIO
ms.assetid: 287996f8-e8ca-4b72-a5f6-016754785c5c
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: CreateDirectoryEx, CreateDirectoryEx function [Files], CreateDirectoryExA, CreateDirectoryExW, _win32_createdirectoryex, base.createdirectoryex, fs.createdirectoryex, winbase/CreateDirectoryEx, winbase/CreateDirectoryExA, winbase/CreateDirectoryExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l2-1-1.dll
-	API-MS-Win-Core-File-l2-1-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	API-Ms-Win-Core-File-Ansi-L2-1-0.dll
-	Kernel32Legacy.dll
api_name:
-	CreateDirectoryEx
-	CreateDirectoryExA
-	CreateDirectoryExW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateDirectoryExW function


## -description


Creates a new directory with the attributes of a specified template directory. If the 
    underlying file system supports security on files and directories, the function applies a specified security 
    descriptor to the new directory. The new directory retains the other attributes of the specified template 
    directory.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/75663b30-5bd9-4de7-8e4f-dc58016c2c40">CreateDirectoryTransacted</a> function.


## -parameters




### -param lpTemplateDirectory [in]

The path of the directory to use as a template when creating the new directory.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CreateDirectoryExW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". The 255 character limit per path segment still applies. See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpNewDirectory [in]

The path of the directory to be created.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CreateDirectoryExW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". The 255 character limit per path segment still applies. See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpSecurityAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> 
       structure. The <b>lpSecurityDescriptor</b> member of the structure specifies a security 
       descriptor for the new directory.

If <i>lpSecurityAttributes</i> is <b>NULL</b>, the directory gets a 
       default security descriptor. The access control lists (ACL) in the default security descriptor for a directory 
       are inherited from its parent directory.

The target file system must support security on files and directories for this parameter to have an effect. 
       This is indicated when <a href="https://msdn.microsoft.com/c80a38e1-319e-4f15-8c8a-9d29075e1709">GetVolumeInformation</a> 
       returns <b>FS_PERSISTENT_ACLS</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible errors include the 
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
        <a href="https://msdn.microsoft.com/7f44f907-cd12-4156-91c0-76e577ae25f6">SHCreateDirectoryEx</a> function.

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
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function with the 
    <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag set. For a code example, see 
    <b>CreateFile</b>.

To support inheritance functions that query the security descriptor of this 
     object can heuristically determine and report that inheritance is in effect. For more information, see 
     <a href="https://msdn.microsoft.com/0aa49b9b-13e3-4ef9-921d-ea47a013e5a1">Automatic Propagation of Inheritable ACEs</a>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/f8ca8b10-c8bd-4285-8a40-dbec4c24729c">CreateDirectory</a>



<a href="https://msdn.microsoft.com/75663b30-5bd9-4de7-8e4f-dc58016c2c40">CreateDirectoryTransacted</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32">Creating and Deleting Directories</a>



<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/d699cdd2-e270-4f17-bdec-6eea25b01578">RemoveDirectory</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

