---
UID: NF:msi.MsiReinstallFeatureA
title: MsiReinstallFeatureA function
author: windows-sdk-content
description: Reinstalls features.
old-location: setup\msireinstallfeature.htm
tech.root: msi
ms.assetid: 0750838d-56c8-449c-b1fd-99c9426beb52
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: MsiReinstallFeature, MsiReinstallFeature function, MsiReinstallFeatureA, MsiReinstallFeatureW, REINSTALLMODE_FILEEQUALVERSION, REINSTALLMODE_FILEEXACT, REINSTALLMODE_FILEMISSING, REINSTALLMODE_FILEOLDERVERSION, REINSTALLMODE_FILEREPLACE, REINSTALLMODE_FILEVERIFY, REINSTALLMODE_MACHINEDATA, REINSTALLMODE_PACKAGE, REINSTALLMODE_SHORTCUT, REINSTALLMODE_USERDATA, _msi_msireinstallfeature, msi/MsiReinstallFeature, msi/MsiReinstallFeatureA, msi/MsiReinstallFeatureW, setup.msireinstallfeature
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiReinstallFeatureW (Unicode) and MsiReinstallFeatureA (ANSI)
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
 - MsiReinstallFeature
 - MsiReinstallFeatureA
 - MsiReinstallFeatureW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiReinstallFeatureA function


## -description


The 
<b>MsiReinstallFeature</b> function reinstalls features.


## -parameters




### -param szProduct [in]

Specifies the product code for the product that contains the feature to be reinstalled.


### -param szFeature [in]

Specifies the feature to be reinstalled. The parent feature or child feature of the specified feature is not reinstalled. To reinstall the parent or child feature, you must call the <b>MsiReinstallFeature</b>   function for each separately or use the <a href="https://msdn.microsoft.com/ad69868e-d653-417d-b902-d0d62e05c985">MsiReinstallProduct</a> function.


### -param dwReinstallMode [in]

Specifies what to install. This parameter can be one or more of the following values.

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
Verify the checksum values, and reinstall the file if they are missing or corrupt. This flag only repairs files that have msidbFileAttributesChecksum in the Attributes column of the 
<a href="https://msdn.microsoft.com/31d0e727-a9eb-4cd2-a211-ea7b138d0173">File table</a>.

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
<a href="https://msdn.microsoft.com/809ffd02-cf97-42d8-aed9-c13a14dcd8b4">Registry Table</a> that go to the<b>HKEY_CURRENT_USER</b></p>  or <b>HKEY_USERS</b></p> registry hive.

</td>
</tr>
<tr>
<td width="40%"><a id="REINSTALLMODE_MACHINEDATA"></a><a id="reinstallmode_machinedata"></a><dl>
<dt><b>REINSTALLMODE_MACHINEDATA</b></dt>
</dl>
</td>
<td width="60%">
Rewrite all required registry entries from the 
<a href="https://msdn.microsoft.com/809ffd02-cf97-42d8-aed9-c13a14dcd8b4">Registry Table</a> that go to the <b>HKEY_LOCAL_MACHINE</b></p>or <b>HKEY_CLASSES_ROOT</b></p> registry hive. Rewrite all information from the 
<a href="https://msdn.microsoft.com/0fa00a3f-2a5d-411d-9fc6-9486a600f018">Class Table</a>, 
<a href="https://msdn.microsoft.com/3749095c-f0c0-498c-969f-a6c445cfdd62">Verb Table</a>, 
<a href="https://msdn.microsoft.com/4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4">PublishComponent Table</a>, 
<a href="https://msdn.microsoft.com/66a7e170-6f70-4db7-98f4-8a074471b9f2">ProgID Table</a>, 
<a href="https://msdn.microsoft.com/5d452b24-ae04-4c45-8b3b-48e81f13a21e">MIME Table</a>, 
<a href="https://msdn.microsoft.com/a59c552a-21c0-4dd4-9146-88a5f9a22962">Icon Table</a>, 
<a href="https://msdn.microsoft.com/924858b7-8956-4636-b7c7-c902aa822ee1">Extension Table</a>, and 
<a href="https://msdn.microsoft.com/d76ed6df-944b-4996-bf07-e42ceb7a1b69">AppID Table</a> regardless of machine or user assignment. Reinstall all 
<a href="https://msdn.microsoft.com/1d37e2c4-3ee0-42d2-95de-6e058319a4d4">qualified components</a>.

When reinstalling an application,  this option runs the <a href="https://msdn.microsoft.com/374450bb-316c-4fe6-abb1-cd8a8a31f284">RegisterTypeLibraries</a> and <a href="https://msdn.microsoft.com/fbcf1fdc-5aef-4431-93fe-3ed02748b5ff">InstallODBC</a> actions.

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
Use to run from the source package and re-cache the local package. Do not use  for the first installation of an application or feature.

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
<dt><b>ERROR_UNKNOWN_FEATURE</b></dt>
</dl>
</td>
<td width="60%">
The feature ID does not identify a known feature.

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
<a href="https://msdn.microsoft.com/0153a21f-9b26-4088-b12b-96c9e6918cc3">Displayed Error Messages</a>.
						
					




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Installation and Configuration Functions</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>



<a href="https://msdn.microsoft.com/756d2899-2cfe-473a-bebf-a7f7bbe7d229">REINSTALLMODE Property</a>
 

 

