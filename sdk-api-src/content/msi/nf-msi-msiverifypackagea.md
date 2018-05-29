---
UID: NF:msi.MsiVerifyPackageA
title: MsiVerifyPackageA function
author: windows-sdk-content
description: The MsiVerifyPackage function verifies that the given file is an installation package.
old-location: setup\msiverifypackage.htm
old-project: Msi
ms.assetid: f5b48e5e-cafb-4ab8-8c14-0af5784f2ca6
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: MsiVerifyPackage, MsiVerifyPackage function, MsiVerifyPackageA, MsiVerifyPackageW, _msi_msiverifypackage, msi/MsiVerifyPackage, msi/MsiVerifyPackageA, msi/MsiVerifyPackageW, setup.msiverifypackage
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
req.unicode-ansi: MsiVerifyPackageW (Unicode) and MsiVerifyPackageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRM_LICENSE_ACQ_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
-	Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
-	MsiVerifyPackage
-	MsiVerifyPackageA
-	MsiVerifyPackageW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiVerifyPackageA function


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




