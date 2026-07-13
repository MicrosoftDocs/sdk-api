---
UID: NF:winbase.OpenEncryptedFileRawW
title: OpenEncryptedFileRawW function (winbase.h)
description: Opens an encrypted file in order to backup (export) or restore (import) the file. (Unicode)
helpviewer_keywords: ["CREATE_FOR_DIR", "CREATE_FOR_IMPORT", "OVERWRITE_HIDDEN", "OpenEncryptedFileRaw", "OpenEncryptedFileRaw function [Files]", "OpenEncryptedFileRawW", "base.openencryptedfileraw", "fs.openencryptedfileraw", "winbase/OpenEncryptedFileRaw", "winbase/OpenEncryptedFileRawW"]
old-location: fs\openencryptedfileraw.htm
tech.root: fs
ms.assetid: f792f38d-783e-4f39-a9d8-0c378d508d97
ms.date: 12/05/2018
ms.keywords: CREATE_FOR_DIR, CREATE_FOR_IMPORT, OVERWRITE_HIDDEN, OpenEncryptedFileRaw, OpenEncryptedFileRaw function [Files], OpenEncryptedFileRawA, OpenEncryptedFileRawW, base.openencryptedfileraw, fs.openencryptedfileraw, winbase/OpenEncryptedFileRaw, winbase/OpenEncryptedFileRawA, winbase/OpenEncryptedFileRawW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenEncryptedFileRawW (Unicode) and OpenEncryptedFileRawA (ANSI)
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
 - OpenEncryptedFileRawW
 - winbase/OpenEncryptedFileRawW
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
 - OpenEncryptedFileRaw
 - OpenEncryptedFileRawA
 - OpenEncryptedFileRawW
req.apiset: ext-ms-win-advapi32-encryptedfile-l1-1-0 (introduced in Windows 8)
---

# OpenEncryptedFileRawW function


## -description

Opens an encrypted file in order to backup (export) or restore (import)
the file.  This is one of a group of Encrypted File System (EFS) functions that is intended  to implement backup and restore functionality, while maintaining files in their encrypted state.

## -parameters

### -param lpFileName [in]

The name of the file to be opened. The string must consist of characters from the Windows character set.

### -param ulFlags [in]

The operation to be performed. This parameter may be one of the
         following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Open the file for export
                                     (backup).

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_FOR_IMPORT"></a><a id="create_for_import"></a><dl>
<dt><b>CREATE_FOR_IMPORT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The file is being opened for import
                                     (restore).

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_FOR_DIR"></a><a id="create_for_dir"></a><dl>
<dt><b>CREATE_FOR_DIR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Import (restore) a directory containing encrypted files.  This must be combined with one of the previous two flags to indicate the operation.

</td>
</tr>
<tr>
<td width="40%"><a id="OVERWRITE_HIDDEN"></a><a id="overwrite_hidden"></a><dl>
<dt><b>OVERWRITE_HIDDEN</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Overwrite a hidden file on import.

</td>
</tr>
</table>

### -param pvContext [out]

The address of a  context
         block that must be presented in subsequent calls to 
         <a href="/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw">ReadEncryptedFileRaw</a>, <a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>, or 
         <a href="/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw">CloseEncryptedFileRaw</a>.  Do not modify it.

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns a nonzero error code defined in
      WinError.h. You can use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the
      <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a generic text description of
      the error.

## -remarks

The caller must either have read or write access to the file, or it must have backup privilege <a href="/windows/desktop/SecAuthZ/authorization-constants">SeBackupPrivilege</a> on the machine on which the files reside in order for the call to succeed.

To back up an encrypted file, call <b>OpenEncryptedFileRaw</b> to open the
      file and then call <a href="/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw">ReadEncryptedFileRaw</a>. When the backup is
      complete, call <a href="/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw">CloseEncryptedFileRaw</a>.

To restore an encrypted file, call <b>OpenEncryptedFileRaw</b>, specifying
      <b>CREATE_FOR_IMPORT</b> in the <i>ulFlags</i> parameter, and then call
      <a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a> once. When the operation is completed, call
      <a href="/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw">CloseEncryptedFileRaw</a>.

<b>OpenEncryptedFileRaw</b> fails if <i>lpFileName</i> exceeds <b>MAX_PATH</b> characters when opening an encrypted file on a remote machine.

 If the caller does not have access to the key for the file, the caller needs <a href="/windows/desktop/SecAuthZ/authorization-constants">SeBackupPrivilege</a> to export encrypted files or SeRestorePrivilege to import encrypted files.


The  <a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a> and <a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a> functions handle backup and restore of unencrypted files.

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





> [!NOTE]
> The winbase.h header defines OpenEncryptedFileRaw as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a>



<a href="/windows/desktop/api/winbase/nf-winbase-backupwrite">BackupWrite</a>



<a href="/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw">CloseEncryptedFileRaw</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw">ReadEncryptedFileRaw</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw">WriteEncryptedFileRaw</a>
