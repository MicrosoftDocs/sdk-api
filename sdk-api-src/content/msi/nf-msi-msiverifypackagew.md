---
UID: NF:msi.MsiVerifyPackageW
title: MsiVerifyPackageW function (msi.h)
description: The MsiVerifyPackage function verifies that the given file is an installation package. (Unicode)
helpviewer_keywords: ["MsiVerifyPackage", "MsiVerifyPackage function", "MsiVerifyPackageW", "_msi_msiverifypackage", "msi/MsiVerifyPackage", "msi/MsiVerifyPackageW", "setup.msiverifypackage"]
old-location: setup\msiverifypackage.htm
tech.root: setup
ms.assetid: f5b48e5e-cafb-4ab8-8c14-0af5784f2ca6
ms.date: 12/05/2018
ms.keywords: MsiVerifyPackage, MsiVerifyPackage function, MsiVerifyPackageA, MsiVerifyPackageW, _msi_msiverifypackage, msi/MsiVerifyPackage, msi/MsiVerifyPackageA, msi/MsiVerifyPackageW, setup.msiverifypackage
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiVerifyPackageW (Unicode) and MsiVerifyPackageA (ANSI)
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
 - MsiVerifyPackageW
 - msi/MsiVerifyPackageW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
 - MsiVerifyPackage
 - MsiVerifyPackageA
 - MsiVerifyPackageW
---

# MsiVerifyPackageW function


## -description

The 
<b>MsiVerifyPackage</b> function verifies that the given file is an installation package.

## -parameters

### -param szPackagePath [in]

Specifies the path and file name of the package.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_PACKAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The file is not a valid package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_PACKAGE_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The file could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The file is a package.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

> [!NOTE]
> The msi.h header defines MsiVerifyPackage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

