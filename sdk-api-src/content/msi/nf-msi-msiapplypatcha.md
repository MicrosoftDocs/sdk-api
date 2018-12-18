---
UID: NF:msi.MsiApplyPatchA
title: MsiApplyPatchA function
author: windows-sdk-content
description: For each product listed by the patch package as eligible to receive the patch, the MsiApplyPatch function invokes an installation and sets the PATCH property to the path of the patch package.
old-location: setup\msiapplypatch.htm
tech.root: msi
ms.assetid: c78006ad-7355-49b6-8e79-a98dcdb0e54f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INSTALLTYPE_DEFAULT, INSTALLTYPE_NETWORK_IMAGE, INSTALLTYPE_SINGLE_INSTANCE, MsiApplyPatch, MsiApplyPatch function, MsiApplyPatchA, MsiApplyPatchW, _msi_msiapplypatch, msi/MsiApplyPatch, msi/MsiApplyPatchA, msi/MsiApplyPatchW, setup.msiapplypatch
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiApplyPatchW (Unicode) and MsiApplyPatchA (ANSI)
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
 - MsiApplyPatch
 - MsiApplyPatchA
 - MsiApplyPatchW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiApplyPatchA function


## -description


For each product listed by the patch package as eligible to receive the patch, the 
<b>MsiApplyPatch</b> function invokes an installation and sets the 
<a href="https://msdn.microsoft.com/f2993544-2124-4fb0-8bb3-59f5d8e76b83">PATCH</a> property to the path of the patch package.
		


## -parameters




### -param szPatchPackage [in]

A null-terminated string specifying the full path to the patch package.


### -param szInstallPackage [in]

If <i>eInstallType</i> is set to INSTALLTYPE_NETWORK_IMAGE, this parameter is a null-terminated string that specifies a path to the product that is to be patched. The installer applies the patch to every eligible product listed in the patch package if <i>szInstallPackage</i> is set to null and <i>eInstallType</i> is set to INSTALLTYPE_DEFAULT.

If <i>eInstallType</i> is INSTALLTYPE_SINGLE_INSTANCE, the installer applies the patch to the product specified by <i>szInstallPackage</i>. In this case, other eligible products listed in the patch package are ignored and the <i>szInstallPackage</i> parameter contains the null-terminated string representing the product code of the instance to patch. This type of installation requires the installer running Windows Server 2003 or Windows XP.


### -param eInstallType [in]

This parameter specifies the type of installation to patch.

<table>
<tr>
<th>Type of installation</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLTYPE_NETWORK_IMAGE"></a><a id="installtype_network_image"></a><dl>
<dt><b>INSTALLTYPE_NETWORK_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
Specifies an administrative installation. In this case, <i>szInstallPackage</i> must be set to a package path. A value of 1 for INSTALLTYPE_NETWORK_IMAGE sets this for an administrative installation.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLTYPE_DEFAULT"></a><a id="installtype_default"></a><dl>
<dt><b>INSTALLTYPE_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Searches system for products to patch. In this case, <i>szInstallPackage</i> must be 0.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLTYPE_SINGLE_INSTANCE"></a><a id="installtype_single_instance"></a><dl>
<dt><b>INSTALLTYPE_SINGLE_INSTANCE</b></dt>
</dl>
</td>
<td width="60%">
Patch the product specified by <i>szInstallPackage</i>. <i>szInstallPackage</i> is the product code of the instance to patch. This type of installation requires the installer running Windows Server 2003 or Windows XP with SP1. For more information see, <a href="https://msdn.microsoft.com/5147ecbd-c395-4a8f-972d-f5c5b2173eff">Installing Multiple Instances of Products and Patches</a>.

</td>
</tr>
</table>
 


### -param szCommandLine [in]

A null-terminated string that specifies command line property settings. See About 
<a href="https://msdn.microsoft.com/b7b715e7-e92c-4b84-b60d-a0ff8412749b">Properties</a> and 
<a href="https://msdn.microsoft.com/ec2626fa-a3be-45e5-a566-658206d3d0bb">Setting Public Property Values on the Command Line</a>. See the Remarks section.


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
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Patch package could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The patch package is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The patch package is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>An error relating to an action</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="https://msdn.microsoft.com/9ea81ef3-a5b5-4d13-b0b8-3da6e919315e">Error Codes</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a></b></dt>
</dl>
</td>
<td width="60%">
An initialization error occurred.

</td>
</tr>
</table>
 




## -remarks



Because the list delimiter for transforms, sources, and patches is a semicolon, this character should not be used for file names or paths.

<div class="alert"><b>Note</b>  <p class="note">You must set the <a href="https://msdn.microsoft.com/14346fef-7923-4f30-bca8-96a29c0f820d">REINSTALL</a> property on the command line when applying a <a href="https://msdn.microsoft.com/c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98">small update</a> or <a href="https://msdn.microsoft.com/74c962f9-93cd-40ed-a8fe-141ccac79d79">minor upgrade</a> patch. Without this property, the patch is registered on the system but cannot update files.  For patches that do not use a <a href="https://msdn.microsoft.com/cdad16ad-426c-4e04-8003-b32c67be7329">Custom Action Type 51</a> to automatically set the <b>REINSTALL</b> and <a href="https://msdn.microsoft.com/756d2899-2cfe-473a-bebf-a7f7bbe7d229">REINSTALLMODE</a> properties, the <b>REINSTALL</b> property must be explicitly set with the <i>szCommandLine</i> parameter. Set the <b>REINSTALL</b> property to list the features affected by the patch, or use a practical default setting of "REINSTALL=ALL". The default value of the <b>REINSTALLMODE</b> property is "omus". Beginning with Windows Installer version 3.0, the <b>REINSTALL</b> property is configured by the installer and does not need to be set on the command line.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9ea81ef3-a5b5-4d13-b0b8-3da6e919315e">Error Codes</a>



<a href="https://msdn.microsoft.com/5cce27ff-1143-4fe6-b4bd-727581431c07">Initialization Error</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>



<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>
 

 

