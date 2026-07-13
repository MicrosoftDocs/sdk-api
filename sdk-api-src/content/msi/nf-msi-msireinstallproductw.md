---
UID: NF:msi.MsiReinstallProductW
title: MsiReinstallProductW function (msi.h)
description: Reinstalls products. (Unicode)
helpviewer_keywords: ["MsiReinstallProduct", "MsiReinstallProduct function", "MsiReinstallProductW", "REINSTALLMODE_FILEEQUALVERSION", "REINSTALLMODE_FILEEXACT", "REINSTALLMODE_FILEMISSING", "REINSTALLMODE_FILEOLDERVERSION", "REINSTALLMODE_FILEREPLACE", "REINSTALLMODE_FILEVERIFY", "REINSTALLMODE_MACHINEDATA", "REINSTALLMODE_PACKAGE", "REINSTALLMODE_SHORTCUT", "REINSTALLMODE_USERDATA", "_msi_msireinstallproduct", "msi/MsiReinstallProduct", "msi/MsiReinstallProductW", "setup.msireinstallproduct"]
old-location: setup\msireinstallproduct.htm
tech.root: setup
ms.assetid: ad69868e-d653-417d-b902-d0d62e05c985
ms.date: 12/05/2018
ms.keywords: MsiReinstallProduct, MsiReinstallProduct function, MsiReinstallProductA, MsiReinstallProductW, REINSTALLMODE_FILEEQUALVERSION, REINSTALLMODE_FILEEXACT, REINSTALLMODE_FILEMISSING, REINSTALLMODE_FILEOLDERVERSION, REINSTALLMODE_FILEREPLACE, REINSTALLMODE_FILEVERIFY, REINSTALLMODE_MACHINEDATA, REINSTALLMODE_PACKAGE, REINSTALLMODE_SHORTCUT, REINSTALLMODE_USERDATA, _msi_msireinstallproduct, msi/MsiReinstallProduct, msi/MsiReinstallProductA, msi/MsiReinstallProductW, setup.msireinstallproduct
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiReinstallProductW (Unicode) and MsiReinstallProductA (ANSI)
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
 - MsiReinstallProductW
 - msi/MsiReinstallProductW
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
 - MsiReinstallProduct
 - MsiReinstallProductA
 - MsiReinstallProductW
---

# MsiReinstallProductW function


## -description

The 
<b>MsiReinstallProduct</b> function reinstalls products.

## -parameters

### -param szProduct [in]

Specifies the product code for the product to be reinstalled.

### -param szReinstallMode [in]

Specifies the reinstall mode. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_FILEMISSING"></a><a id="reinstallmode_filemissing"></a><dl>
<dt><b>REINSTALLMODE_FILEMISSING</b></dt>
</dl>
</td>
<td width="60%">
Reinstall only if the file is missing.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_FILEOLDERVERSION"></a><a id="reinstallmode_fileolderversion"></a><dl>
<dt><b>REINSTALLMODE_FILEOLDERVERSION</b></dt>
</dl>
</td>
<td width="60%">
Reinstall if the file is missing or is an older version.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_FILEEQUALVERSION"></a><a id="reinstallmode_fileequalversion"></a><dl>
<dt><b>REINSTALLMODE_FILEEQUALVERSION</b></dt>
</dl>
</td>
<td width="60%">
Reinstall if the file is missing, or is an equal or older version.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_FILEEXACT"></a><a id="reinstallmode_fileexact"></a><dl>
<dt><b>REINSTALLMODE_FILEEXACT</b></dt>
</dl>
</td>
<td width="60%">
Reinstall if the file is missing or is a different version.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_FILEVERIFY"></a><a id="reinstallmode_fileverify"></a><dl>
<dt><b>REINSTALLMODE_FILEVERIFY</b></dt>
</dl>
</td>
<td width="60%">
Verify the checksum values and reinstall the file if they are missing or corrupt. This flag only repairs files that have msidbFileAttributesChecksum in the Attributes column of the 
<a href="/windows/desktop/Msi/file-table">File table</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_FILEREPLACE"></a><a id="reinstallmode_filereplace"></a><dl>
<dt><b>REINSTALLMODE_FILEREPLACE</b></dt>
</dl>
</td>
<td width="60%">
Force all files to be reinstalled, regardless of checksum or version.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_USERDATA"></a><a id="reinstallmode_userdata"></a><dl>
<dt><b>REINSTALLMODE_USERDATA</b></dt>
</dl>
</td>
<td width="60%">
Rewrite all required registry entries from the 
<a href="/windows/desktop/Msi/registry-table">Registry Table</a> that go to the <b>HKEY_CURRENT_USER</b></p>  or <b>HKEY_USERS</b></p> registry hive.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_MACHINEDATA"></a><a id="reinstallmode_machinedata"></a><dl>
<dt><b>REINSTALLMODE_MACHINEDATA</b></dt>
</dl>
</td>
<td width="60%">
Rewrite all required registry entries from the 
<a href="/windows/desktop/Msi/registry-table">Registry Table</a> that go to the <b>HKEY_LOCAL_MACHINE</b></p> or <b>HKEY_CLASSES_ROOT</b></p> registry hive. Rewrite all information from the 
<a href="/windows/desktop/Msi/class-table">Class Table</a>, 
<a href="/windows/desktop/Msi/verb-table">Verb Table</a>, 
<a href="/windows/desktop/Msi/publishcomponent-table">PublishComponent Table</a>, 
<a href="/windows/desktop/Msi/progid-table">ProgID Table</a>, 
<a href="/windows/desktop/Msi/mime-table">MIMET Table</a>, 
<a href="/windows/desktop/Msi/icon-table">Icon Table</a>, 
<a href="/windows/desktop/Msi/extension-table">Extension Table</a>, and 
<a href="/windows/desktop/Msi/appid-table">AppID Table</a> regardless of machine or user assignment. Reinstall all 
<a href="/windows/desktop/api/msi/nf-msi-msiprovidequalifiedcomponenta">qualified components</a>.

When reinstalling an application,  this option runs the <a href="/windows/desktop/Msi/registertypelibraries-action">RegisterTypeLibraries</a> and <a href="/windows/desktop/Msi/installodbc-action">InstallODBC</a> actions.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_SHORTCUT"></a><a id="reinstallmode_shortcut"></a><dl>
<dt><b>REINSTALLMODE_SHORTCUT</b></dt>
</dl>
</td>
<td width="60%">
Reinstall all shortcuts and re-cache all icons overwriting any existing shortcuts and icons.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_PACKAGE"></a><a id="reinstallmode_package"></a><dl>
<dt><b>REINSTALLMODE_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
Use to run from the source package and re-cache the local package. Do not use for the first installation of an application or feature.

</td>
</tr>
</table>

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SERVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The installation service could not be accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SUSPEND</b></dt>
</dl>
</td>
<td width="60%">
The installation was suspended and is incomplete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_USEREXIT</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the installation.

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
The product code does not identify a known product.

</td>
</tr>
</table>
 

For more information, see 
<a href="/windows/desktop/Msi/displayed-error-messages">Displayed Error Messages</a>.

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Installation and Configuration Functions</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple Package Installations</a>



<a href="/windows/desktop/Msi/reinstallmode">REINSTALLMODE Property</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiReinstallProduct as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
