---
UID: NF:msiquery.MsiGetTargetPathW
title: MsiGetTargetPathW function (msiquery.h)
description: The MsiGetTargetPath function returns the full target path for a folder in the Directory table. (Unicode)
helpviewer_keywords: ["MsiGetTargetPath", "MsiGetTargetPath function", "MsiGetTargetPathW", "_msi_msigettargetpath", "msiquery/MsiGetTargetPath", "msiquery/MsiGetTargetPathW", "setup.msigettargetpath"]
old-location: setup\msigettargetpath.htm
tech.root: setup
ms.assetid: cad0e1c1-3f3a-4438-8b85-ea146c943579
ms.date: 12/05/2018
ms.keywords: MsiGetTargetPath, MsiGetTargetPath function, MsiGetTargetPathA, MsiGetTargetPathW, _msi_msigettargetpath, msiquery/MsiGetTargetPath, msiquery/MsiGetTargetPathA, msiquery/MsiGetTargetPathW, setup.msigettargetpath
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetTargetPathW (Unicode) and MsiGetTargetPathA (ANSI)
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
 - MsiGetTargetPathW
 - msiquery/MsiGetTargetPathW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiGetTargetPath
 - MsiGetTargetPathA
 - MsiGetTargetPathW
---

# MsiGetTargetPathW function


## -description

The 
<b>MsiGetTargetPath</b> function returns the full target path for a folder in the 
<a href="/windows/desktop/Msi/directory-table">Directory table</a>.

## -parameters

### -param hInstall [in]

Handle to the installation provided to a DLL custom action or obtained through <a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>.

### -param szFolder [in]

A null-terminated string that specifies a record of the 
<a href="/windows/desktop/Msi/directory-table">Directory table</a>. If the directory is a root directory, this can be a value from the DefaultDir column. Otherwise it must be a value from the Directory column.

### -param szPathBuf [out]

Pointer to the buffer that receives the null terminated full target path. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szPathBuf</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function then returns ERROR_MORE_DATA and <i>pcchPathBuf</i> contains the required buffer size in TCHARs, not including the terminating null character. On return of ERROR_SUCCESS, <i>pcchPathBuf</i> contains the number of TCHARs written to the buffer, not including the terminating null character.

### -param pcchPathBuf [in, out]

Pointer to the variable that specifies the size, in <b>TCHARs</b>, of the buffer pointed to by the variable <i>szPathBuf</i> When the function returns ERROR_SUCCESS, this variable contains the size of the data copied to <i>szPathBuf</i>, not including the terminating null character. If <i>szPathBuf</i> is not large enough, the function returns ERROR_MORE_DATA and stores the required size, not including the terminating null character, in the variable pointed to by <i>pcchPathBuf</i>.

## -returns

The 
<b>MsiGetTargetPath</b> function returns the following values:

## -remarks

If ERROR_MORE_DATA is returned, the parameter which is a pointer gives the size of the buffer required to hold the string. If ERROR_SUCCESS is returned, it gives the number of characters written to the string buffer. Therefore you can get the size of the buffer by passing in an empty string (for example "") for the parameter that specifies the buffer. Do not attempt to determine the size of the buffer by passing in a Null (value=0).

Before calling this function, the installer must first run the 
<a href="/windows/desktop/Msi/costinitialize-action">CostInitialize action</a>, 
<a href="/windows/desktop/Msi/filecost-action">FileCost action</a>, and 
<a href="/windows/desktop/Msi/costfinalize-action">CostFinalize action</a>. For more information, see <a href="/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions from Programs</a>.

<b>MsiGetTargetPath</b> returns the default path of the target directory authored in the package if the target's current location is unavailable for an installation. For example, if during a 
<a href="/windows/desktop/Msi/maintenance-installation">Maintenance Installation</a> a target directory at a network location is unavailable, the installer resets the target directory paths back to their defaults. To get the actual path of the target directory in this case call 
<a href="/windows/desktop/api/msi/nf-msi-msiprovidecomponenta">MsiProvideComponent</a> for a component that is known to have been previously installed into the searched for directory and set <i>dwInstallMode</i> to INSTALLMODE_NODETECTION.

For more information, see 
<a href="/windows/desktop/Msi/calling-database-functions-from-programs">Calling Database Functions From Programs</a>.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiGetTargetPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Installer Location Functions</a>



<a href="/windows/desktop/Msi/passing-null-as-the-argument-of-windows-installer-functions">Passing Null as the Argument of Windows Installer Functions</a>
