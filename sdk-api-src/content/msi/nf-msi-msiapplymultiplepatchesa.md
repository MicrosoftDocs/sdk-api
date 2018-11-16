---
UID: NF:msi.MsiApplyMultiplePatchesA
title: MsiApplyMultiplePatchesA function
author: windows-sdk-content
description: Applies one or more patches to products eligible to receive the patches.
old-location: setup\msiapplymultiplepatches.htm
tech.root: Msi
ms.assetid: dc0a93e3-9f3c-40b2-86ee-98306038742a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MsiApplyMultiplePatches, MsiApplyMultiplePatches function, MsiApplyMultiplePatchesA, MsiApplyMultiplePatchesW, msi/MsiApplyMultiplePatches, msi/MsiApplyMultiplePatchesA, msi/MsiApplyMultiplePatchesW, setup.msiapplymultiplepatches
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
req.unicode-ansi: MsiApplyMultiplePatchesW (Unicode) and MsiApplyMultiplePatchesA (ANSI)
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
 - MsiApplyMultiplePatches
 - MsiApplyMultiplePatchesA
 - MsiApplyMultiplePatchesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MsiApplyMultiplePatchesA
: 
---

# MsiApplyMultiplePatchesA function


## -description


The <b>MsiApplyMultiplePatches</b> function applies one or more patches to products eligible to receive the patches. 
   The <b>MsiApplyMultiplePatches</b> function sets the <a href="https://msdn.microsoft.com/f2993544-2124-4fb0-8bb3-59f5d8e76b83">PATCH</a> property with a list of patches delimited by semicolons and invokes the patching of the target products. Other properties can be set using a properties list.


## -parameters




### -param szPatchPackages [in]

A  semicolon-delimited list of the paths to patch files as a single string. For example: ""c:\sus\download\cache\Office\sp1.msp; c:\sus\download\cache\Office\QFE1.msp; c:\sus\download\cache\Office\QFEn.msp"   "


### -param szProductCode [in, optional]

This parameter is the <a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a> GUID of the product to be patched. The user or application calling <b>MsiApplyMultiplePatches</b> must have privileges to apply patches. When this parameter is <b>NULL</b>, the patches are applied to all eligible products. When this parameter is non-<b>NULL</b>, the patches are applied only to the specified product.


### -param szPropertiesList [in, optional]

A null-terminated string that specifies command–line property settings used during the patching of products. If there are no command–line property settings, pass in a <b>NULL</b> pointer. An empty string is  an invalid parameter. These properties are shared by all  target products. For more information, see  
<a href="https://msdn.microsoft.com/b7b715e7-e92c-4b84-b60d-a0ff8412749b">About Properties</a> and 
<a href="https://msdn.microsoft.com/ec2626fa-a3be-45e5-a566-658206d3d0bb">Setting Public Property Values on the Command Line</a>.

<div class="alert"><b>Note</b>  The properties list should not contain the  <a href="https://msdn.microsoft.com/f2993544-2124-4fb0-8bb3-59f5d8e76b83">PATCH</a> property. If the <b>PATCH</b> property is set in the command line the value is ignored and is overwritten with the patches being applied.</div>
<div> </div>

## -returns



The <b>MsiApplyMultiplePatches</b> function returns the following values.

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
Some arguments passed in are incorrect or contradicting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed and all  products are successfully patched. <b>ERROR_SUCCESS</b> is returned only if all the  products eligible for the patches are patched successfully. If none of the new patches are applicable, <a href="https://msdn.microsoft.com/dc0a93e3-9f3c-40b2-86ee-98306038742a">MsiApplyMultiplePatches</a> returns <b>ERROR_SUCCESS</b> and product state remains unchanged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS_REBOOT_INITIATED</b></dt>
</dl>
</td>
<td width="60%">
The restart initiated by the last transaction terminated this call to <a href="https://msdn.microsoft.com/dc0a93e3-9f3c-40b2-86ee-98306038742a">MsiApplyMultiplePatches</a>. All the target products may not have been patched.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS_REBOOT_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The restart required by the last transaction terminated this call to <a href="https://msdn.microsoft.com/dc0a93e3-9f3c-40b2-86ee-98306038742a">MsiApplyMultiplePatches</a>. All target products may not have been patched.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
One of the patch packages provide could not be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
One of the patch packages provide is not a valid one.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_PACKAGE_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
One of the patch packages is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Any error in Winerror.h</b></dt>
</dl>
</td>
<td width="60%">
Implies possible partial completion or that one or more transactions failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b7b715e7-e92c-4b84-b60d-a0ff8412749b">About Properties</a>



<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple-Package Installations</a>



<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="https://msdn.microsoft.com/f2993544-2124-4fb0-8bb3-59f5d8e76b83">PATCH</a>



<a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a>



<a href="https://msdn.microsoft.com/ec2626fa-a3be-45e5-a566-658206d3d0bb">Setting Public Property Values on the Command Line</a>
 

 

