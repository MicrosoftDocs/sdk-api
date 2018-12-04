---
UID: NF:winefs.EncryptionDisable
title: EncryptionDisable function
author: windows-sdk-content
description: Disables or enables encryption of the specified directory and the files in it.
old-location: fs\encryptiondisable.htm
tech.root: fileio
ms.assetid: 6ff93a90-c1cf-4782-862c-d3d7e294c4b0
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: EncryptionDisable, EncryptionDisable function [Files], _win32_encryptiondisable, base.encryptiondisable, fs.encryptiondisable, winefs/EncryptionDisable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winefs.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - EncryptionDisable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EncryptionDisable function


## -description


Disables or enables encryption of the specified directory and the files in it. It does not 
    affect encryption of subdirectories below the indicated directory.
   


## -parameters




### -param DirPath [in]

The name of the directory for which to enable or 
      disable encryption.


### -param Disable [in]

Indicates whether to disable encryption (<b>TRUE</b>) or enable it 
      (<b>FALSE</b>).


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
      




## -remarks



Under normal circumstances, <a href="https://msdn.microsoft.com/7620e9fa-74d6-4b41-93db-4a562be63202">EncryptFile</a> will not encrypt 
    files and directories with the <b>FILE_ATTRIBUTE_SYSTEM</b> attribute set. It is possible to 
    override the <b>FILE_ATTRIBUTE_SYSTEM</b> attribute and encrypt files. Also, if a file or 
    directory is marked with the <b>FILE_ATTRIBUTE_SYSTEM</b> attribute, it will normally be
    invisible to the user in directory listings and Windows Explorer directory windows. 
    <b>EncryptionDisable</b> disables encryption of directories and files. It does not 
    affect the visibility of files with the <b>FILE_ATTRIBUTE_SYSTEM</b> attribute set.
   

If <b>TRUE</b> is passed in, 
    <b>EncryptionDisable</b> will write the following to the 
    Desktop.ini file in the directory (creating it if necessary):

<pre class="syntax" xml:space="preserve"><code>[Encryption]
Disable=1</code></pre>
If the section already exists but <i>Disable</i> is set to 0, it will be set to 1.

Thereafter, <a href="https://msdn.microsoft.com/7620e9fa-74d6-4b41-93db-4a562be63202">EncryptFile</a> will fail on the 
    directory and the files in it, and the code that 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns will be 
    <b>ERROR_DIR_EFS_DISALLOWED</b>. This function does not affect encryption of subdirectories 
    within the given directory.

The user can also manually add or edit the above lines in the Desktop.ini file and produce the 
    same effect.

<b>EncryptionDisable</b> affects only 
    <a href="https://msdn.microsoft.com/96efe065-de62-4941-811d-610465cd7ef5">FileEncryptionStatus</a> and 
    <a href="https://msdn.microsoft.com/7620e9fa-74d6-4b41-93db-4a562be63202">EncryptFile</a>. After the directory is 
    encrypted, any new files and new subdirectories created without the 
    <b>FILE_ATTRIBUTE_SYSTEM</b> attribute will be encrypted.

If <b>FALSE</b> is passed in, 
    <b>EncryptionDisable</b> will write the following to the 
    Desktop.ini file:

<pre class="syntax" xml:space="preserve"><code>[Encryption]
Disable=0</code></pre>
This means that  file encryption is permitted on the files in that directory.

If you try to use <b>EncryptionDisable</b> to set the 
    directory to the state it is already in, the function succeeds but has no effect.

If you try to use <b>EncryptionDisable</b> to disable or 
    enable encryption on a file, the attempt will fail.

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
 

SMB 3.0 does not support EFS on shares with continuous availability capability.





## -see-also




<a href="https://msdn.microsoft.com/6b8f0ed0-8825-4c84-bf58-3a89cda882b4">DecryptFile</a>



<a href="https://msdn.microsoft.com/7620e9fa-74d6-4b41-93db-4a562be63202">EncryptFile</a>



<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/96efe065-de62-4941-811d-610465cd7ef5">FileEncryptionStatus</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>
 

 

