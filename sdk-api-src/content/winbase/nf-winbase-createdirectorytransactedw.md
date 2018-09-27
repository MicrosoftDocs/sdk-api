---
UID: NF:winbase.CreateDirectoryTransactedW
title: CreateDirectoryTransactedW function
author: windows-sdk-content
description: Creates a new directory as a transacted operation, with the attributes of a specified template directory.
old-location: fs\createdirectorytransacted.htm
tech.root: fileio
ms.assetid: 75663b30-5bd9-4de7-8e4f-dc58016c2c40
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateDirectoryTransacted, CreateDirectoryTransacted function [Files], CreateDirectoryTransactedA, CreateDirectoryTransactedW, fs.createdirectorytransacted, winbase/CreateDirectoryTransacted, winbase/CreateDirectoryTransactedA, winbase/CreateDirectoryTransactedW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDirectoryTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Creates a new directory as a transacted operation, with the attributes of a specified template 
    directory. If the underlying file system supports security on files and directories, the function 
    applies a specified security descriptor to the new directory. The new directory retains the other attributes of 
    the specified template directory.


## -parameters




### -param lpTemplateDirectory [in, optional]

The path of the directory to use as a template when creating the new directory.  This parameter can be 
       <b>NULL</b>.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

The directory must reside on the local computer; otherwise, the function fails and the last error code is set 
       to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param lpNewDirectory [in]

The path of the directory to be created.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.


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


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


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
    <a href="https://msdn.microsoft.com/0cbc081d-8787-409b-84bc-a6a28d8f83a0">CreateFileTransacted</a> function with the 
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




## -see-also




<a href="https://msdn.microsoft.com/0cbc081d-8787-409b-84bc-a6a28d8f83a0">CreateFileTransacted</a>



<a href="https://msdn.microsoft.com/52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32">Creating and Deleting Directories</a>



<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/e8600166-62dc-4398-9e16-43b07f7f0b89">RemoveDirectoryTransacted</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

