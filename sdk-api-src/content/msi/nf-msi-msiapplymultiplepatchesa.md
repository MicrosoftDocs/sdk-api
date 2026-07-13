---
UID: NF:msi.MsiApplyMultiplePatchesA
title: MsiApplyMultiplePatchesA function (msi.h)
description: Applies one or more patches to products eligible to receive the patches. (ANSI)
helpviewer_keywords: ["MsiApplyMultiplePatchesA", "msi/MsiApplyMultiplePatchesA"]
old-location: setup\msiapplymultiplepatches.htm
tech.root: setup
ms.assetid: dc0a93e3-9f3c-40b2-86ee-98306038742a
ms.date: 12/05/2018
ms.keywords: MsiApplyMultiplePatches, MsiApplyMultiplePatches function, MsiApplyMultiplePatchesA, MsiApplyMultiplePatchesW, msi/MsiApplyMultiplePatches, msi/MsiApplyMultiplePatchesA, msi/MsiApplyMultiplePatchesW, setup.msiapplymultiplepatches
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiApplyMultiplePatchesA
 - msi/MsiApplyMultiplePatchesA
dev_langs:
 - c++
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
---

# MsiApplyMultiplePatchesA function


## -description

The <b>MsiApplyMultiplePatches</b> function applies one or more patches to products eligible to receive the patches. 
   The <b>MsiApplyMultiplePatches</b> function sets the <a href="/windows/desktop/Msi/patch">PATCH</a> property with a list of patches delimited by semicolons and invokes the patching of the target products. Other properties can be set using a properties list.

## -parameters

### -param szPatchPackages [in]

A  semicolon-delimited list of the paths to patch files as a single string. For example: ""c:\sus\download\cache\Office\sp1.msp; c:\sus\download\cache\Office\QFE1.msp; c:\sus\download\cache\Office\QFEn.msp"   "

### -param szProductCode [in, optional]

This parameter is the <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID of the product to be patched. The user or application calling <b>MsiApplyMultiplePatches</b> must have privileges to apply patches. When this parameter is <b>NULL</b>, the patches are applied to all eligible products. When this parameter is non-<b>NULL</b>, the patches are applied only to the specified product.

### -param szPropertiesList [in, optional]

A null-terminated string that specifies command–line property settings used during the patching of products. If there are no command–line property settings, pass in a <b>NULL</b> pointer. An empty string is  an invalid parameter. These properties are shared by all  target products. For more information, see  
<a href="/windows/desktop/Msi/about-properties">About Properties</a> and 
<a href="/windows/desktop/Msi/setting-public-property-values-on-the-command-line">Setting Public Property Values on the Command Line</a>.

<div class="alert"><b>Note</b>  The properties list should not contain the  <a href="/windows/desktop/Msi/patch">PATCH</a> property. If the <b>PATCH</b> property is set in the command line the value is ignored and is overwritten with the patches being applied.</div>
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
The function completed and all  products are successfully patched. <b>ERROR_SUCCESS</b> is returned only if all the  products eligible for the patches are patched successfully. If none of the new patches are applicable, <a href="/windows/desktop/api/msi/nf-msi-msiapplymultiplepatchesa">MsiApplyMultiplePatches</a> returns <b>ERROR_SUCCESS</b> and product state remains unchanged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS_REBOOT_INITIATED</b></dt>
</dl>
</td>
<td width="60%">
The restart initiated by the last transaction terminated this call to <a href="/windows/desktop/api/msi/nf-msi-msiapplymultiplepatchesa">MsiApplyMultiplePatches</a>. All the target products may not have been patched.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS_REBOOT_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The restart required by the last transaction terminated this call to <a href="/windows/desktop/api/msi/nf-msi-msiapplymultiplepatchesa">MsiApplyMultiplePatches</a>. All target products may not have been patched.

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

<a href="/windows/desktop/Msi/about-properties">About Properties</a>



<a href="/windows/desktop/Msi/multiple-package-installations">Multiple-Package Installations</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/patch">PATCH</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>



<a href="/windows/desktop/Msi/setting-public-property-values-on-the-command-line">Setting Public Property Values on the Command Line</a>

## -remarks

> [!NOTE]
> The msi.h header defines MsiApplyMultiplePatches as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
