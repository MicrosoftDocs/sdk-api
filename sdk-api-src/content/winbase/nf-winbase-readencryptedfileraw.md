---
UID: NF:winbase.ReadEncryptedFileRaw
title: ReadEncryptedFileRaw function (winbase.h)
description: Backs up (export) encrypted files.
helpviewer_keywords: ["ReadEncryptedFileRaw","ReadEncryptedFileRaw function [Files]","base.readencryptedfileraw","fs.readencryptedfileraw","winbase/ReadEncryptedFileRaw"]
old-location: fs\readencryptedfileraw.htm
tech.root: fs
ms.assetid: 15f6f617-969d-4a40-9038-b902a3c2518b
ms.date: 12/05/2018
ms.keywords: ReadEncryptedFileRaw, ReadEncryptedFileRaw function [Files], base.readencryptedfileraw, fs.readencryptedfileraw, winbase/ReadEncryptedFileRaw
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReadEncryptedFileRaw
 - winbase/ReadEncryptedFileRaw
dev_langs:
 - c++
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
 - ReadEncryptedFileRaw
req.apiset: ext-ms-win-advapi32-encryptedfile-l1-1-0 (introduced in Windows 8)
---

# ReadEncryptedFileRaw function


## -description

Backs up (export) encrypted files.  This is one of a group of Encrypted File System (EFS) 
    functions that is intended  to implement backup and restore functionality, while maintaining files in their 
    encrypted state.

## -parameters

### -param pfExportCallback [in]

A pointer to the export callback function. The system calls the callback function multiple times, each time 
      passing a block of the file's data to the callback function until the entire file has been read. For more 
      information, see <a href="/windows/desktop/api/winbase/nc-winbase-pfe_export_func">ExportCallback</a>.

### -param pvCallbackContext [in, optional]

A pointer to an application-defined and allocated context block. The system passes this pointer to the 
      callback function as a parameter so that the callback function can have access to application-specific data. 
      This can be a structure and can contain any data the application needs, such as the handle to the file that will 
      contain the backup copy of the encrypted file.

### -param pvContext [in]

A pointer to a system-defined context block. The context block is returned by the 
      <a href="/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa">OpenEncryptedFileRaw</a> function. Do not modify 
      it.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, it returns a nonzero error code defined in WinError.h. You can use 
       <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the 
       <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a generic text description of the error.

## -remarks

The file being backed up is not decrypted;  it is backed up in its encrypted state.

To back up an encrypted file, call 
     <a href="/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa">OpenEncryptedFileRaw</a> to open the file. Then call 
     <b>ReadEncryptedFileRaw</b>, passing it the address of an 
     application-defined export callback function. The system calls this callback function multiple times until the 
     entire file's contents have been read and backed up.  When the backup is complete, call 
     <a href="/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw">CloseEncryptedFileRaw</a> to free resources and close 
     the file. See <a href="/windows/desktop/api/winbase/nc-winbase-pfe_export_func">ExportCallback</a> for details about how to 
     declare the export callback function.

To restore an encrypted file, call 
     <a href="/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa">OpenEncryptedFileRaw</a>, specifying 
     <b>CREATE_FOR_IMPORT</b> in the <i>ulFlags</i> parameter. Then call 
     <a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>, passing it the address of 
     an application-defined import callback function. The system calls this callback function multiple times until the 
     entire file's contents have been read and restored. When the restore is complete, call 
     <a href="/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw">CloseEncryptedFileRaw</a> to free resources and close 
     the file. See <a href="/windows/desktop/api/winbase/nc-winbase-pfe_import_func">ImportCallback</a> for details about how to 
     declare the import callback function.

This function is intended for the backup of only encrypted files; see 
    <a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a> for backup of unencrypted files.

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

<a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a>



<a href="/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw">CloseEncryptedFileRaw</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa">OpenEncryptedFileRaw</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>
