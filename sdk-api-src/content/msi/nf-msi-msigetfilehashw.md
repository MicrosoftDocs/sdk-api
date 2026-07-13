---
UID: NF:msi.MsiGetFileHashW
title: MsiGetFileHashW function (msi.h)
description: The MsiGetFileHash function takes the path to a file and returns a 128-bit hash of that file. Authoring tools may use MsiGetFileHash to obtain the file hash needed to populate the MsiFileHash table. (Unicode)
helpviewer_keywords: ["MsiGetFileHash", "MsiGetFileHash function", "MsiGetFileHashW", "_msi_msigetfilehash", "msi/MsiGetFileHash", "msi/MsiGetFileHashW", "setup.msigetfilehash"]
old-location: setup\msigetfilehash.htm
tech.root: setup
ms.assetid: afd9f0b4-432f-4d23-b59d-7406ac2f68bb
ms.date: 12/05/2018
ms.keywords: MsiGetFileHash, MsiGetFileHash function, MsiGetFileHashA, MsiGetFileHashW, _msi_msigetfilehash, msi/MsiGetFileHash, msi/MsiGetFileHashA, msi/MsiGetFileHashW, setup.msigetfilehash
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetFileHashW (Unicode) and MsiGetFileHashA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiGetFileHashW
 - msi/MsiGetFileHashW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiGetFileHash
 - MsiGetFileHashA
 - MsiGetFileHashW
---

# MsiGetFileHashW function


## -description

The 
<b>MsiGetFileHash</b> function takes the path to a file and returns a 128-bit hash of that file. Authoring tools may use 
<b>MsiGetFileHash</b> to obtain the file hash needed to populate the 
<a href="/windows/desktop/Msi/msifilehash-table">MsiFileHash table</a>.

Windows Installer uses file hashing as a means to detect and eliminate unnecessary file copying. A file hash stored in the MsiFileHash table may be compared to a hash of an existing file on the user's computer.

## -parameters

### -param szFilePath [in]

Path to file that is to be hashed.

### -param dwOptions [in]

The value in this column must be 0. This parameter is reserved for future use.

### -param pHash [out]

Pointer to the returned file hash information.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The file could not be opened to get version information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error has occurred.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The entire 128-bit file hash is returned as four 32-bit fields. The numbering of the four fields is zero-based. The values returned by 
<b>MsiGetFileHash</b> correspond to the four fields of the 
<a href="/windows/desktop/api/msi/ns-msi-msifilehashinfo">MSIFILEHASHINFO</a> structure. The first field corresponds to the HashPart1 column of the MsiFileHash table, the second field corresponds to the HashPart2 column, the third field corresponds to the HashPart3 column, and the fourth field corresponds to the HashPart4 column.

The hash information entered into the MsiFileHash table must be obtained by calling 
<b>MsiGetFileHash</b> or the 
<a href="/windows/desktop/Msi/installer-filehash">FileHash</a> method. Do not attempt to use other methods to generate the file hash.





> [!NOTE]
> The msi.h header defines MsiGetFileHash as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/default-file-versioning">Default File Versioning</a>



<a href="/windows/desktop/api/msi/ns-msi-msifilehashinfo">MSIFILEHASHINFO</a>



<a href="/windows/desktop/Msi/msifilehash-table">MsiFileHash table</a>
