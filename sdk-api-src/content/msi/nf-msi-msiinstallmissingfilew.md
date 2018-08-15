---
UID: NF:msi.MsiInstallMissingFileW
title: MsiInstallMissingFileW function
author: windows-sdk-content
description: The MsiInstallMissingFile function installs files that are unexpectedly missing.
old-location: setup\msiinstallmissingfile.htm
old-project: msi
ms.assetid: 289ce1e2-64ac-4222-9d0d-52c8fdd4f9c3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MsiInstallMissingFile, MsiInstallMissingFile function, MsiInstallMissingFileA, MsiInstallMissingFileW, _msi_msiinstallmissingfile, msi/MsiInstallMissingFile, msi/MsiInstallMissingFileA, msi/MsiInstallMissingFileW, setup.msiinstallmissingfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msi.h
req.include-header: 
req.redist: 
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
 - MsiInstallMissingFile
 - MsiInstallMissingFileA
 - MsiInstallMissingFileW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiInstallMissingFileW function


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
<a href="https://msdn.microsoft.com/0153a21f-9b26-4088-b12b-96c9e6918cc3">Displayed Error Messages</a>.




## -remarks



The 
<b>MsiInstallMissingFile</b> function obtains the component that the file belongs to from the file table. Then, the product feature that requires the least additional disk space is installed.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Installation and Configuration Functions</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>
 

 

