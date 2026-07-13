---
UID: NF:msi.MsiGetFileVersionA
title: MsiGetFileVersionA function (msi.h)
description: The MsiGetFileVersion returns the version string and language string in the format that the installer expects to find them in the database. (ANSI)
helpviewer_keywords: ["MsiGetFileVersionA", "msi/MsiGetFileVersionA"]
old-location: setup\msigetfileversion.htm
tech.root: setup
ms.assetid: 9dd7d71e-2e76-4755-a979-f3dcdcd6ebec
ms.date: 12/05/2018
ms.keywords: MsiGetFileVersion, MsiGetFileVersion function, MsiGetFileVersionA, MsiGetFileVersionW, _msi_msigetfileversion, msi/MsiGetFileVersion, msi/MsiGetFileVersionA, msi/MsiGetFileVersionW, setup.msigetfileversion
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetFileVersionW (Unicode) and MsiGetFileVersionA (ANSI)
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
 - MsiGetFileVersionA
 - msi/MsiGetFileVersionA
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
 - MsiGetFileVersion
 - MsiGetFileVersionA
 - MsiGetFileVersionW
---

# MsiGetFileVersionA function


## -description

The 
<b>MsiGetFileVersion</b> returns the version string and language string in the format that the installer expects to find them in the database. If you want only version information, set <i>lpLangBuf</i> and <i>pcchLangBuf</i> to 0 (zero). If you just want language information, set <i>lpVersionBuf</i> and <i>pcchVersionBuf</i> to 0 (zero).

## -parameters

### -param szFilePath [in]

Specifies the path to the file.

### -param lpVersionBuf [out]

Returns the file version. 

Set to 0 for language information only.

### -param pcchVersionBuf [in, out]

In and out buffer count as the number of <b>TCHAR</b>. 

Set to 0 (zero) for language information only. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.

### -param lpLangBuf [out]

Returns the file language. 

Set to 0 (zero) for version information only.

### -param pcchLangBuf [in, out]

In and out buffer count as the number of <b>TCHAR</b>. 

Set to 0 (zero) for version information only. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character.

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
Successful completion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
File does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
File cannot be opened to get version information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
File does not contain version information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The version information is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiGetFileVersion as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
