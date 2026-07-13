---
UID: NF:msi.MsiInstallMissingFileA
title: MsiInstallMissingFileA function (msi.h)
description: The MsiInstallMissingFile function installs files that are unexpectedly missing. (ANSI)
helpviewer_keywords: ["MsiInstallMissingFileA", "msi/MsiInstallMissingFileA"]
old-location: setup\msiinstallmissingfile.htm
tech.root: setup
ms.assetid: 289ce1e2-64ac-4222-9d0d-52c8fdd4f9c3
ms.date: 12/05/2018
ms.keywords: MsiInstallMissingFile, MsiInstallMissingFile function, MsiInstallMissingFileA, MsiInstallMissingFileW, _msi_msiinstallmissingfile, msi/MsiInstallMissingFile, msi/MsiInstallMissingFileA, msi/MsiInstallMissingFileW, setup.msiinstallmissingfile
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiInstallMissingFileW (Unicode) and MsiInstallMissingFileA (ANSI)
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
 - MsiInstallMissingFileA
 - msi/MsiInstallMissingFileA
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
 - MsiInstallMissingFile
 - MsiInstallMissingFileA
 - MsiInstallMissingFileW
---

# MsiInstallMissingFileA function


## -description

The 
<b>MsiInstallMissingFile</b> function installs files that are unexpectedly missing.

## -parameters

### -param szProduct [in]

Specifies the product code for the product that owns the file to be installed.

### -param szFile [in]

Specifies the file to be installed.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration information is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The installation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SOURCE_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
The source was unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SUSPEND</b></dt>
</dl>
</td>
<td width="60%">
The installation was suspended.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_USEREXIT</b></dt>
</dl>
</td>
<td width="60%">
The user exited the installation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter was invalid.

</td>
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
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product code is unrecognized.

</td>
</tr>
</table>
 

For more information about error messages, see 
<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>.

## -remarks

The 
<b>MsiInstallMissingFile</b> function obtains the component that the file belongs to from the file table. Then, the product feature that requires the least additional disk space is installed.





> [!NOTE]
> The msi.h header defines MsiInstallMissingFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Installation and Configuration Functions</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>
