---
UID: NF:msi.MsiOpenPackageW
title: MsiOpenPackageW function (msi.h)
description: The MsiOpenPackage function opens a package to use with the functions that access the product database. (Unicode)
helpviewer_keywords: ["MsiOpenPackage", "MsiOpenPackage function", "MsiOpenPackageW", "_msi_msiopenpackage", "msi/MsiOpenPackage", "msi/MsiOpenPackageW", "setup.msiopenpackage"]
old-location: setup\msiopenpackage.htm
tech.root: setup
ms.assetid: 1227493a-58dc-4e41-b6d7-9ecce0b3df40
ms.date: 12/05/2018
ms.keywords: MsiOpenPackage, MsiOpenPackage function, MsiOpenPackageA, MsiOpenPackageW, _msi_msiopenpackage, msi/MsiOpenPackage, msi/MsiOpenPackageA, msi/MsiOpenPackageW, setup.msiopenpackage
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiOpenPackageW (Unicode) and MsiOpenPackageA (ANSI)
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
 - MsiOpenPackageW
 - msi/MsiOpenPackageW
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
 - MsiOpenPackage
 - MsiOpenPackageA
 - MsiOpenPackageW
---

# MsiOpenPackageW function


## -description

The 
<b>MsiOpenPackage</b> function opens a package to use with the functions that access the product database. The 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a> function must be called with the handle when the handle is not needed. <div class="alert"><b>Note</b>  Initialize COM on the same thread before calling the  <b>MsiOpenPackage</b>, <a href="/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a> function.</div>
<div> </div>

## -parameters

### -param szPackagePath [in]

The path to the package.

### -param hProduct [out]

A pointer to a variable that receives the product handle.

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
The product could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_REMOTE_PROHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Windows Installer does not permit installation from a remote desktop connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completes successfully.

</td>
</tr>
</table>
 

If this function fails, it may return a system error code. For more information, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

MsiOpenPackage can accept an opened database handle in the form "#nnnn", where nnnn is the database handle in string form, i.e. #123, instead of a path to the package. This is intended for development tasks such as running validation actions, or for use with database management tools.





> [!NOTE]
> The msi.h header defines MsiOpenPackage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Product Query Functions</a>
