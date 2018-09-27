---
UID: NF:winbase.CloseEncryptedFileRaw
title: CloseEncryptedFileRaw function
author: windows-sdk-content
description: Closes an encrypted file after a backup or restore operation, and frees associated system resources.
old-location: fs\closeencryptedfileraw.htm
tech.root: fileio
ms.assetid: 54bf7114-0ebb-4d9c-bc67-2ac351dbe55d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CloseEncryptedFileRaw, CloseEncryptedFileRaw function [Files], base.closeencryptedfileraw, fs.closeencryptedfileraw, winbase/CloseEncryptedFileRaw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
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
 - Ext-MS-Win-AdvAPI32-EncryptedFile-l1-1-0.dll
 - Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-1.dll
api_name:
 - CloseEncryptedFileRaw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseEncryptedFileRaw function


## -description


Closes an encrypted file after a backup 
or restore operation, and frees associated system resources. This is one of a group of Encrypted File System (EFS) functions that is intended  to implement backup and restore functionality, while maintaining files in their encrypted state.


## -parameters




### -param pvContext [in]

A pointer to a system-defined context block. The
         <a href="https://msdn.microsoft.com/f792f38d-783e-4f39-a9d8-0c378d508d97">OpenEncryptedFileRaw</a> function returns the context block.


## -returns



This function does not return a value.




## -remarks



The <b>CloseEncryptedFileRaw</b> function frees allocated system resources
      such as the system-defined context block and closes the file.

The  <a href="https://msdn.microsoft.com/47d13662-af70-4c76-9fb6-3835e329ae5f">BackupRead</a> and <a href="https://msdn.microsoft.com/92befb48-68eb-4af3-b58a-c5e17bf14098">BackupWrite</a> functions handle backup and restore of unencrypted files.

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
 

Note that SMB 3.0 does not support EFS on shares with continuous availability capability.




## -see-also




<a href="https://msdn.microsoft.com/47d13662-af70-4c76-9fb6-3835e329ae5f">BackupRead</a>



<a href="https://msdn.microsoft.com/92befb48-68eb-4af3-b58a-c5e17bf14098">BackupWrite</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/f792f38d-783e-4f39-a9d8-0c378d508d97">OpenEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/f44e291e-dbc6-4a44-92ba-92a81e043764">WriteEncryptedFileRaw</a>
 

 

