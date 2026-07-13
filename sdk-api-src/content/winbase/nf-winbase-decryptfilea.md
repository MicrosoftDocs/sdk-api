---
UID: NF:winbase.DecryptFileA
title: DecryptFileA function (winbase.h)
description: Decrypts an encrypted file or directory. (ANSI)
helpviewer_keywords: ["DecryptFileA", "winbase/DecryptFileA"]
old-location: fs\decryptfile.htm
tech.root: fs
ms.assetid: 6b8f0ed0-8825-4c84-bf58-3a89cda882b4
ms.date: 12/05/2018
ms.keywords: DecryptFile, DecryptFile function [Files], DecryptFileA, DecryptFileW, _win32_decryptfile, base.decryptfile, fs.decryptfile, winbase/DecryptFile, winbase/DecryptFileA, winbase/DecryptFileW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DecryptFileA
 - winbase/DecryptFileA
dev_langs:
 - c++
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
req.apiset: ext-ms-win-advapi32-encryptedfile-l1-1-0 (introduced in Windows 8)
---

# DecryptFileA function


## -description

Decrypts an encrypted file or directory.

## -parameters

### -param lpFileName [in]

The name of the file or directory to be decrypted.

The caller must have the <b>FILE_READ_DATA</b>, <b>FILE_WRITE_DATA</b>, <b>FILE_READ_ATTRIBUTES</b>, <b>FILE_WRITE_ATTRIBUTES</b>, and <b>SYNCHRONIZE</b> access rights. For more information, see 
<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param dwReserved

Reserved; must be zero.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>DecryptFile</b> function requires exclusive access to the file being decrypted, and will fail if another process is using the file. If the file is not encrypted, 
<b>DecryptFile</b> simply returns a nonzero value, which indicates success.

If <i>lpFileName</i> specifies a read-only file, the function fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_FILE_READ_ONLY</b>. If <i>lpFileName</i> specifies a directory that contains a read-only file, the functions succeeds but the directory is not decrypted.

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
> The winbase.h header defines DecryptFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-encryptfilea">EncryptFile</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>
