---
UID: NF:winbase.WriteEncryptedFileRaw
title: WriteEncryptedFileRaw function
author: windows-driver-content
description: Restores (import) encrypted files.
old-location: fs\writeencryptedfileraw.htm
old-project: FileIO
ms.assetid: f44e291e-dbc6-4a44-92ba-92a81e043764
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WriteEncryptedFileRaw, WriteEncryptedFileRaw function [Files], base.writeencryptedfileraw, fs.writeencryptedfileraw, winbase/WriteEncryptedFileRaw
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	Ext-MS-Win-AdvAPI32-EncryptedFile-l1-1-0.dll
-	Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-1.dll
api_name:
-	WriteEncryptedFileRaw
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WriteEncryptedFileRaw function


## -description


Restores (import) encrypted files. This is one of a group of Encrypted File System (EFS) 
    functions that is intended  to implement backup and restore functionality, while maintaining files in their 
    encrypted state.


## -parameters




### -param pfImportCallback [in]

A pointer to the import callback function. The system calls the callback function multiple times, each time 
      passing a buffer that will be filled by the callback function with a portion of backed-up file's data. When the 
      callback function signals that the entire file has been processed, it tells the system that the restore 
      operation is finished. For more information, see 
      <a href="https://msdn.microsoft.com/4c951e44-15d8-43c8-bd3d-293a1ec9d444">ImportCallback</a>.


### -param pvCallbackContext [in, optional]

A pointer to an application-defined and allocated context block. The system passes this pointer to the 
      callback function as a parameter so that the callback function can have access to application-specific data. 
      This can be a structure and can contain any data the application needs, such as the handle to the file that will 
      contain the backup copy of the encrypted file.


### -param pvContext [in]

A pointer to a system-defined context block. The context block is returned by the 
      <a href="https://msdn.microsoft.com/f792f38d-783e-4f39-a9d8-0c378d508d97">OpenEncryptedFileRaw</a> function. Do not modify 
      it.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, it returns a nonzero error code defined in WinError.h. You can use 
       <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the 
       <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a generic text description of the error.




## -remarks



The file being restored is not decrypted;  it is restored in its encrypted state.

To back up an encrypted file, call 
     <a href="https://msdn.microsoft.com/f792f38d-783e-4f39-a9d8-0c378d508d97">OpenEncryptedFileRaw</a> to open the file. Then call 
     <a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>, passing it the address of an 
     application-defined export callback function. The system calls this callback function multiple times until the 
     entire file's contents have been read and backed up.  When the backup is complete, call 
     <a href="https://msdn.microsoft.com/54bf7114-0ebb-4d9c-bc67-2ac351dbe55d">CloseEncryptedFileRaw</a> to free resources and close 
     the file. See <a href="https://msdn.microsoft.com/156948c9-d7b4-4491-bdb1-e1864a32caab">ExportCallback</a> for details about how to 
     declare the export callback function.

To restore an encrypted file, call 
     <a href="https://msdn.microsoft.com/f792f38d-783e-4f39-a9d8-0c378d508d97">OpenEncryptedFileRaw</a>, specifying 
     <b>CREATE_FOR_IMPORT</b> in the <i>ulFlags</i> parameter. Then call 
     <b>WriteEncryptedFileRaw</b>, passing it the address of 
     an application-defined import callback function. The system calls this callback function multiple times until the 
     entire file's contents have been read and restored. When the restore is complete, call 
     <a href="https://msdn.microsoft.com/54bf7114-0ebb-4d9c-bc67-2ac351dbe55d">CloseEncryptedFileRaw</a> to free resources and close 
     the file. See <a href="https://msdn.microsoft.com/4c951e44-15d8-43c8-bd3d-293a1ec9d444">ImportCallback</a> for details about how to 
     declare the export callback function.

If the file is a sparse file that was backed up from a volume with a smaller sparse allocation unit size than 
    the volume it is being restored to, the sparse blocks in the middle of the file may not properly align with the 
    larger blocks and the function call would fail and set an <b>ERROR_INVALID_PARAMETER</b> last 
    error code. The sparse allocation unit size is either 16 clusters or 64 KB, whichever is smaller.

This function is intended for restoring only encrypted files; see 
    <a href="https://msdn.microsoft.com/92befb48-68eb-4af3-b58a-c5e17bf14098">BackupWrite</a> for restoring unencrypted files.

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




<a href="https://msdn.microsoft.com/92befb48-68eb-4af3-b58a-c5e17bf14098">BackupWrite</a>



<a href="https://msdn.microsoft.com/54bf7114-0ebb-4d9c-bc67-2ac351dbe55d">CloseEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/4c951e44-15d8-43c8-bd3d-293a1ec9d444">ImportCallback</a>



<a href="https://msdn.microsoft.com/f792f38d-783e-4f39-a9d8-0c378d508d97">OpenEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>
 

 

