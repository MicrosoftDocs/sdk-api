---
UID: NF:msi.MsiGetFileHashA
title: MsiGetFileHashA function
author: windows-sdk-content
description: The MsiGetFileHash function takes the path to a file and returns a 128-bit hash of that file. Authoring tools may use MsiGetFileHash to obtain the file hash needed to populate the MsiFileHash table.
old-location: setup\msigetfilehash.htm
old-project: Msi
ms.assetid: afd9f0b4-432f-4d23-b59d-7406ac2f68bb
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: MsiGetFileHash, MsiGetFileHash function, MsiGetFileHashA, MsiGetFileHashW, _msi_msigetfilehash, msi/MsiGetFileHash, msi/MsiGetFileHashA, msi/MsiGetFileHashW, setup.msigetfilehash
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DRM_LICENSE_ACQ_DATA
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
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiGetFileHashA function


## -description


The 
<b>MsiGetFileHash</b> function takes the path to a file and returns a 128-bit hash of that file. Authoring tools may use 
<b>MsiGetFileHash</b> to obtain the file hash needed to populate the 
<a href="https://msdn.microsoft.com/972a2784-418d-4cb3-b13c-df89b079e94c">MsiFileHash table</a>.

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
<a href="https://msdn.microsoft.com/b4176b5b-149d-4542-9a6c-27281877a3ff">MSIFILEHASHINFO</a> structure. The first field corresponds to the HashPart1 column of the MsiFileHash table, the second field corresponds to the HashPart2 column, the third field corresponds to the HashPart3 column, and the fourth field corresponds to the HashPart4 column.

The hash information entered into the MsiFileHash table must be obtained by calling 
<b>MsiGetFileHash</b> or the 
<a href="https://msdn.microsoft.com/065ffde1-4d7c-4e71-9315-7926d4cd38ed">FileHash</a> method. Do not attempt to use other methods to generate the file hash.




## -see-also




<a href="https://msdn.microsoft.com/a09e091c-ee82-4951-b129-d1d4c8948883">Default File Versioning</a>



<a href="https://msdn.microsoft.com/b4176b5b-149d-4542-9a6c-27281877a3ff">MSIFILEHASHINFO</a>



<a href="https://msdn.microsoft.com/972a2784-418d-4cb3-b13c-df89b079e94c">MsiFileHash table</a>
 

 

