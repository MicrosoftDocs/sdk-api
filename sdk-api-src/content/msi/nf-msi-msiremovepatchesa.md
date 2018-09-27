---
UID: NF:msi.MsiRemovePatchesA
title: MsiRemovePatchesA function
author: windows-sdk-content
description: Removes one or more patches from a single product.
old-location: setup\msiremovepatches.htm
tech.root: msi
ms.assetid: c1d73e52-fd58-4895-822e-3ebc8fe12db7
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: INSTALLTYPE_SINGLE_INSTANCE, MsiRemovePatches, MsiRemovePatches function, MsiRemovePatchesA, MsiRemovePatchesW, msi/MsiRemovePatches, msi/MsiRemovePatchesA, msi/MsiRemovePatchesW, setup.msiremovepatches, setup.msiuninstallpatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiRemovePatchesW (Unicode) and MsiRemovePatchesA (ANSI)
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
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiRemovePatches
 - MsiRemovePatchesA
 - MsiRemovePatchesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiRemovePatchesA function


## -description


The <b>MsiRemovePatches</b> function removes  one or more patches from a single product. To remove a patch from multiple products, <b>MsiRemovePatches</b> must be called for each product.


## -parameters




### -param szPatchList [in]

A null-terminated string that represents the list of patches to remove.  Each patch can be specified by the GUID of the patch or the full path to the patch package. The patches in the list are delimited by semicolons.


### -param szProductCode [in]

A null-terminated string that is the <a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a> (GUID) of the product from which the patches are removed.  This parameter cannot be <b>NULL</b>.


### -param eUninstallType [in]

Value that indicates the type of patch removal to perform. This parameter must be <b>INSTALLTYPE_SINGLE_INSTANCE</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLTYPE_SINGLE_INSTANCE"></a><a id="installtype_single_instance"></a><dl>
<dt><b>INSTALLTYPE_SINGLE_INSTANCE</b></dt>
</dl>
</td>
<td width="60%">
The patch is uninstalled for only the product specified by <i>szProduct</i>.

</td>
</tr>
</table>
 


### -param szPropertyList [in, optional]

A null-terminated string that specifies command-line property settings. For more information see  
<a href="https://msdn.microsoft.com/b7b715e7-e92c-4b84-b60d-a0ff8412749b">About Properties</a> and 
<a href="https://msdn.microsoft.com/ec2626fa-a3be-45e5-a566-658206d3d0bb">Setting Public Property Values on the Command Line</a>. This parameter can be <b>NULL</b>.


## -returns



The <b>MsiRemovePatches</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was included.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The patch package could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The patch was successfully removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product specified by <i>szProductList</i> is not installed either per-machine or per-user for the caller of <a href="https://msdn.microsoft.com/c1d73e52-fd58-4895-822e-3ebc8fe12db7">MsiRemovePatches</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The patch package could not be opened.

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
The patch package cannot be processed by this version of the Windows Installer service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_REMOVAL_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The patch package is not removable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PATCH</b></dt>
</dl>
</td>
<td width="60%">
The patch has not been applied to this product.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_REMOVAL_DISALLOWED</b></dt>
</dl>
</td>
<td width="60%">
Patch removal was disallowed by policy.

</td>
</tr>
</table>
 




## -remarks



See  <a href="https://msdn.microsoft.com/11e995b7-30c7-4992-b436-3af289ac3966">Uninstalling Patches</a> for an example that demonstrates how an application can remove a patch from all products that are available to the user. 




## -see-also




<a href="https://msdn.microsoft.com/b7b715e7-e92c-4b84-b60d-a0ff8412749b">About Properties</a>



<a href="https://msdn.microsoft.com/c78006ad-7355-49b6-8e79-a98dcdb0e54f">MsiApplyPatch</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>



<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a>



<a href="https://msdn.microsoft.com/2ad30ac9-eac9-49cf-98ae-5c053a0b500a">Removing Patches</a>



<a href="https://msdn.microsoft.com/ec2626fa-a3be-45e5-a566-658206d3d0bb">Setting Public Property Values on the Command Line</a>



<a href="https://msdn.microsoft.com/11e995b7-30c7-4992-b436-3af289ac3966">Uninstalling Patches</a>
 

 

