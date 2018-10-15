---
UID: NF:winbase.DecryptFileW
title: DecryptFileW function
author: windows-sdk-content
description: Decrypts an encrypted file or directory.
old-location: fs\decryptfile.htm
tech.root: FileIO
ms.assetid: 6b8f0ed0-8825-4c84-bf58-3a89cda882b4
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DecryptFile, DecryptFile function [Files], DecryptFileA, DecryptFileW, _win32_decryptfile, base.decryptfile, fs.decryptfile, winbase/DecryptFile, winbase/DecryptFileA, winbase/DecryptFileW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DecryptFileW (Unicode) and DecryptFileA (ANSI)
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
 - Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-0.dll
 - Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-1.dll
api_name:
 - DecryptFile
 - DecryptFileA
 - DecryptFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DecryptFileW function


## -description


Decrypts an encrypted file or directory.


## -parameters




### -param lpFileName [in]

The name of the file or directory to be decrypted.

The caller must have the <b>FILE_READ_DATA</b>, <b>FILE_WRITE_DATA</b>, <b>FILE_READ_ATTRIBUTES</b>, <b>FILE_WRITE_ATTRIBUTES</b>, and <b>SYNCHRONIZE</b> access rights. For more information, see 
<a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>.


### -param dwReserved

Reserved; must be zero.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>DecryptFile</b> function requires exclusive access to the file being decrypted, and will fail if another process is using the file. If the file is not encrypted, 
<b>DecryptFile</b> simply returns a nonzero value, which indicates success.

If <i>lpFileName</i> specifies a read-only file, the function fails and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_FILE_READ_ONLY</b>. If <i>lpFileName</i> specifies a directory that contains a read-only file, the functions succeeds but the directory is not decrypted.

In Windows 8, Windows Server 2012, and later, this function is supported by the following technologies.

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




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/7620e9fa-74d6-4b41-93db-4a562be63202">EncryptFile</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>
 

 

