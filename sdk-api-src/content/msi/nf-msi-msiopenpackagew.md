---
UID: NF:msi.MsiOpenPackageW
title: MsiOpenPackageW function (msi.h)
description: The MsiOpenPackage function opens a package to use with the functions that access the product database.
old-location: setup\msiopenpackage.htm
tech.root: Msi
ms.assetid: 1227493a-58dc-4e41-b6d7-9ecce0b3df40
ms.date: 12/05/2018
ms.keywords: MsiOpenPackage, MsiOpenPackage function, MsiOpenPackageA, MsiOpenPackageW, _msi_msiopenpackage, msi/MsiOpenPackage, msi/MsiOpenPackageA, msi/MsiOpenPackageW, setup.msiopenpackage
ms.topic: function
f1_keywords:
- msi/MsiOpenPackage
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiOpenPackageW function


## -description


The 
<b>MsiOpenPackage</b> function opens a package to use with the functions that access the product database. The 
<a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a> function must be called with the handle when the handle is not needed. <div class="alert"><b>Note</b>  Initialize COM on the same thread before calling the  <b>MsiOpenPackage</b>, <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenpackageexa">MsiOpenPackageEx</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a> function.</div>
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
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



MsiOpenPackage can accept an opened database handle in the form "#nnnn", where nnnn is the database handle in string form, i.e. #123, instead of a path to the package. This is intended for development tasks such as running validation actions, or for use with database management tools.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/installer-function-reference">Product Query Functions</a>
 

 

