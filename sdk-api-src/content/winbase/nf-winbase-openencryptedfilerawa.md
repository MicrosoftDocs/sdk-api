---
UID: NF:winbase.OpenEncryptedFileRawA
title: OpenEncryptedFileRawA function
author: windows-sdk-content
description: Opens an encrypted file in order to backup (export) or restore (import) the file.
old-location: fs\openencryptedfileraw.htm
tech.root: fileio
ms.assetid: f792f38d-783e-4f39-a9d8-0c378d508d97
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CREATE_FOR_DIR, CREATE_FOR_IMPORT, OVERWRITE_HIDDEN, OpenEncryptedFileRaw, OpenEncryptedFileRaw function [Files], OpenEncryptedFileRawA, OpenEncryptedFileRawW, base.openencryptedfileraw, fs.openencryptedfileraw, winbase/OpenEncryptedFileRaw, winbase/OpenEncryptedFileRawA, winbase/OpenEncryptedFileRawW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenEncryptedFileRawA function


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
         <a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>, <a href="https://msdn.microsoft.com/f44e291e-dbc6-4a44-92ba-92a81e043764">WriteEncryptedFileRaw</a>, or 
         <a href="https://msdn.microsoft.com/54bf7114-0ebb-4d9c-bc67-2ac351dbe55d">CloseEncryptedFileRaw</a>.  Do not modify it.


## -returns



If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns a nonzero error code defined in
      WinError.h. You can use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the
      <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a generic text description of
      the error.




## -remarks



The caller must either have read or write access to the file, or it must have backup privilege <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeBackupPrivilege</a> on the machine on which the files reside in order for the call to succeed.

To back up an encrypted file, call <b>OpenEncryptedFileRaw</b> to open the
      file and then call <a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>. When the backup is
      complete, call <a href="https://msdn.microsoft.com/54bf7114-0ebb-4d9c-bc67-2ac351dbe55d">CloseEncryptedFileRaw</a>.

To restore an encrypted file, call <b>OpenEncryptedFileRaw</b>, specifying
      <b>CREATE_FOR_IMPORT</b> in the <i>ulFlags</i> parameter, and then call
      <a href="https://msdn.microsoft.com/f44e291e-dbc6-4a44-92ba-92a81e043764">WriteEncryptedFileRaw</a> once. When the operation is completed, call
      <a href="https://msdn.microsoft.com/54bf7114-0ebb-4d9c-bc67-2ac351dbe55d">CloseEncryptedFileRaw</a>.

<b>OpenEncryptedFileRaw</b> fails if <i>lpFileName</i> exceeds <b>MAX_PATH</b> characters when opening an encrypted file on a remote machine.

 If the caller does not have access to the key for the file, the caller needs <a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">SeBackupPrivilege</a> to export encrypted files or SeRestorePrivilege to import encrypted files.


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
 

SMB 3.0 does not support EFS on shares with continuous availability capability.




## -see-also




<a href="https://msdn.microsoft.com/47d13662-af70-4c76-9fb6-3835e329ae5f">BackupRead</a>



<a href="https://msdn.microsoft.com/92befb48-68eb-4af3-b58a-c5e17bf14098">BackupWrite</a>



<a href="https://msdn.microsoft.com/54bf7114-0ebb-4d9c-bc67-2ac351dbe55d">CloseEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/15f6f617-969d-4a40-9038-b902a3c2518b">ReadEncryptedFileRaw</a>



<a href="https://msdn.microsoft.com/f44e291e-dbc6-4a44-92ba-92a81e043764">WriteEncryptedFileRaw</a>
 

 

