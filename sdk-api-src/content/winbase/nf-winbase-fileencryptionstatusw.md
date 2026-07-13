---
UID: NF:winbase.FileEncryptionStatusW
title: FileEncryptionStatusW function (winbase.h)
description: Retrieves the encryption status of the specified file. (Unicode)
helpviewer_keywords: ["FILE_ENCRYPTABLE", "FILE_IS_ENCRYPTED", "FILE_READ_ONLY", "FILE_ROOT_DIR", "FILE_SYSTEM_ATTR", "FILE_SYSTEM_DIR", "FILE_SYSTEM_NOT_SUPPORT", "FILE_UNKNOWN", "FILE_USER_DISALLOWED", "FileEncryptionStatus", "FileEncryptionStatus function [Files]", "FileEncryptionStatusW", "_win32_fileencryptionstatus", "base.fileencryptionstatus", "fs.fileencryptionstatus", "winbase/FileEncryptionStatus", "winbase/FileEncryptionStatusW"]
old-location: fs\fileencryptionstatus.htm
tech.root: fs
ms.assetid: 96efe065-de62-4941-811d-610465cd7ef5
ms.date: 12/05/2018
ms.keywords: FILE_ENCRYPTABLE, FILE_IS_ENCRYPTED, FILE_READ_ONLY, FILE_ROOT_DIR, FILE_SYSTEM_ATTR, FILE_SYSTEM_DIR, FILE_SYSTEM_NOT_SUPPORT, FILE_UNKNOWN, FILE_USER_DISALLOWED, FileEncryptionStatus, FileEncryptionStatus function [Files], FileEncryptionStatusA, FileEncryptionStatusW, _win32_fileencryptionstatus, base.fileencryptionstatus, fs.fileencryptionstatus, winbase/FileEncryptionStatus, winbase/FileEncryptionStatusA, winbase/FileEncryptionStatusW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FileEncryptionStatusW (Unicode) and FileEncryptionStatusA (ANSI)
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
 - FileEncryptionStatusW
 - winbase/FileEncryptionStatusW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - FileEncryptionStatus
 - FileEncryptionStatusA
 - FileEncryptionStatusW
---

# FileEncryptionStatusW function


## -description

Retrieves the encryption status of the specified file.

## -parameters

### -param lpFileName [in]

The name of the file.

### -param lpStatus [out]

A pointer to a variable that receives the encryption status of the file. This parameter can be one of the 
      following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_ENCRYPTABLE"></a><a id="file_encryptable"></a><dl>
<dt><b>FILE_ENCRYPTABLE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The file can be encrypted.
        

<b>Home, Home Premium, Starter, and ARM Editions of Windows:  </b><b>FILE_ENCRYPTABLE</b> may be returned but EFS does not support encrypting files on 
          these editions of Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_IS_ENCRYPTED"></a><a id="file_is_encrypted"></a><dl>
<dt><b>FILE_IS_ENCRYPTED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The file is encrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_READ_ONLY"></a><a id="file_read_only"></a><dl>
<dt><b>FILE_READ_ONLY</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The file is a read-only file.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ROOT_DIR"></a><a id="file_root_dir"></a><dl>
<dt><b>FILE_ROOT_DIR</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The file is a root directory. Root directories cannot be encrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SYSTEM_ATTR"></a><a id="file_system_attr"></a><dl>
<dt><b>FILE_SYSTEM_ATTR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The file is a system file. System files cannot be encrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SYSTEM_DIR"></a><a id="file_system_dir"></a><dl>
<dt><b>FILE_SYSTEM_DIR</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The file is a system directory. System directories cannot be encrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SYSTEM_NOT_SUPPORT"></a><a id="file_system_not_support"></a><dl>
<dt><b>FILE_SYSTEM_NOT_SUPPORT</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The file system does not support file encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_UNKNOWN"></a><a id="file_unknown"></a><dl>
<dt><b>FILE_UNKNOWN</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The encryption status is unknown. The file may be encrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_USER_DISALLOWED"></a><a id="file_user_disallowed"></a><dl>
<dt><b>FILE_USER_DISALLOWED</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

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






> [!NOTE]
> The winbase.h header defines FileEncryptionStatus as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-encryptfilea">EncryptFile</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>
