---
UID: NF:fileapi.CreateDirectoryA
title: CreateDirectoryA function
author: windows-sdk-content
description: Creates a new directory.
old-location: fs\createdirectory.htm
tech.root: fileio
ms.assetid: f8ca8b10-c8bd-4285-8a40-dbec4c24729c
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: CreateDirectory, CreateDirectory function [Files], CreateDirectoryA, CreateDirectoryW, _win32_createdirectory, base.createdirectory, fileapi/CreateDirectory, fileapi/CreateDirectoryA, fileapi/CreateDirectoryW, fs.createdirectory, winbase/CreateDirectory, winbase/CreateDirectoryA, winbase/CreateDirectoryW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDirectoryA function


## -description


Creates a new directory. If the underlying file system supports security on files and 
    directories, the function applies a specified security descriptor to the new directory.

To specify a template directory, use the 
    <a href="https://msdn.microsoft.com/287996f8-e8ca-4b72-a5f6-016754785c5c">CreateDirectoryEx</a> function.

To perform this 
    operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/75663b30-5bd9-4de7-8e4f-dc58016c2c40">CreateDirectoryTransacted</a> function.


## -parameters




### -param lpPathName [in]

The path of the directory to be created.

For the ANSI version of this function, there is a default string size limit for paths of 248 characters (<b>MAX_PATH</b> - enough room for a 8.3 filename). To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>


<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>CreateDirectoryW</b>), you can opt-in to remove the 248 character limitation without prepending "\\?\". The 255 character limit per path segment still applies. See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpSecurityAttributes [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> 
       structure. The <b>lpSecurityDescriptor</b> member of the structure specifies a security 
       descriptor for the new directory. If <i>lpSecurityAttributes</i> is 
       <b>NULL</b>, the directory gets a default security descriptor. The ACLs in the default 
       security descriptor for a  directory are inherited from its parent directory.

The target file system must support security on files and directories for this parameter to have an effect. 
       (This is indicated when <a href="https://msdn.microsoft.com/c80a38e1-319e-4f15-8c8a-9d29075e1709">GetVolumeInformation</a> 
       returns <b>FS_PERSISTENT_ACLS</b>.)


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
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
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> with the 
    <b>FILE_FLAG_BACKUP_SEMANTICS</b> flag set. For a code example, see 
    <b>CreateFile</b>.

To support inheritance functions that query the security descriptor of this object may heuristically determine 
    and report that inheritance is in effect. See 
    <a href="https://msdn.microsoft.com/0aa49b9b-13e3-4ef9-921d-ea47a013e5a1">Automatic Propagation of Inheritable ACEs</a> 
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
     <a href="https://msdn.microsoft.com/f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075">Retrieving and Changing File Attributes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/287996f8-e8ca-4b72-a5f6-016754785c5c">CreateDirectoryEx</a>



<a href="https://msdn.microsoft.com/75663b30-5bd9-4de7-8e4f-dc58016c2c40">CreateDirectoryTransacted</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32">Creating and Deleting Directories</a>



<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/d699cdd2-e270-4f17-bdec-6eea25b01578">RemoveDirectory</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a>
 

 

