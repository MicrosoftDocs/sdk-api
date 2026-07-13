---
UID: NF:msi.MsiDetermineApplicablePatchesW
title: MsiDetermineApplicablePatchesW function (msi.h)
description: The MsiDetermineApplicablePatches function takes a set of patch files, XML files, and XML blobs and determines which patches apply to a specified Windows Installer package and in what sequence. (Unicode)
helpviewer_keywords: ["MsiDetermineApplicablePatches", "MsiDetermineApplicablePatches function", "MsiDetermineApplicablePatchesW", "msi/MsiDetermineApplicablePatches", "msi/MsiDetermineApplicablePatchesW", "setup.msidetermineapplicablepatches"]
old-location: setup\msidetermineapplicablepatches.htm
tech.root: setup
ms.assetid: 2362d1dd-695e-48a3-b8ef-4516952ed253
ms.date: 12/05/2018
ms.keywords: MsiDetermineApplicablePatches, MsiDetermineApplicablePatches function, MsiDetermineApplicablePatchesA, MsiDetermineApplicablePatchesW, msi/MsiDetermineApplicablePatches, msi/MsiDetermineApplicablePatchesA, msi/MsiDetermineApplicablePatchesW, setup.msidetermineapplicablepatches
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer 3.0 or later on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDetermineApplicablePatchesW (Unicode) and MsiDetermineApplicablePatchesA (ANSI)
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
 - MsiDetermineApplicablePatchesW
 - msi/MsiDetermineApplicablePatchesW
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
 - MsiDetermineApplicablePatches
 - MsiDetermineApplicablePatchesA
 - MsiDetermineApplicablePatchesW
---

# MsiDetermineApplicablePatchesW function


## -description

The <b>MsiDetermineApplicablePatches</b> function takes a set  of patch files, XML files, and XML blobs and determines which patches apply to a specified Windows Installer  package and in what sequence. The function can account for  superseded or obsolete patches. This function does not account for products or patches that are installed on the system that are not specified in the set.

## -parameters

### -param szProductPackagePath [in]

Full path to an .msi file. The function determines the patches that are applicable to this package and in what sequence.

### -param cPatchInfo [in]

Number of patches in the array. Must be greater than zero.

### -param pPatchInfo [in]

Pointer to an array of <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structures.

## -returns

The 
					<b>MsiDetermineApplicablePatches</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function failed in a manner not covered in the other error codes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATCH_NO_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
No valid sequence could be found for the set of patches.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The patches were successfully sorted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The .msi file was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The path to the .msi file was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PATCH_XML</b></dt>
</dl>
</td>
<td width="60%">
The XML patch data is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_PACKAGE_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An installation package referenced by path cannot be opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This error can be returned if the function was called from a <a href="/windows/desktop/Msi/custom-actions">custom action</a>  or if MSXML 3.0 is not installed. 

</td>
</tr>
</table>

## -remarks

If this function is called from a custom action it fails and returns ERROR_CALL_NOT_IMPLEMENTED.  The function requires MSXML version 3.0 to process XML and returns ERROR_CALL_NOT_IMPLEMENTED if MSXML 3.0 is not installed.


The <b>MsiDetermineApplicablePatches</b> function sets the <b>uStatus</b> and <b>dwOrder</b> members of each <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structure pointed to by <i>pPatchInfo</i>. Each structure contains information about a particular patch.

If the function succeeds, the <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structure of every patch that can be applied  to the product returns with a  <b>uStatus</b> of ERROR_SUCCESS and a <b>dwOrder</b> greater than or equal to zero. The values of <b>dwOrder</b>  greater than or equal to zero indicate the best application sequence for the patches starting with zero.

If the function succeeds, patches excluded from the best patching sequence return a <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structure with a <b>dwOrder</b> equal to -1.  In these cases, a <b>uStatus</b> field of  ERROR_SUCCESS indicates a patch that is  obsolete or superseded for the product.   A <b>uStatus</b> field of ERROR_PATCH_TARGET_NOT_FOUND indicates a patch that is inapplicable to the product.

If the function fails, the <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structure for every patch  returns a  <b>dwOrder</b> equal to -1.  In this case, the <b>uStatus</b> fields  can contain errors with more information about individual patches. For example, ERROR_PATCH_NO_SEQUENCE is returned for patches that have circular sequencing information.





> [!NOTE]
> The msi.h header defines MsiDetermineApplicablePatches as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/msi/nf-msi-msideterminepatchsequencea">MsiDeterminePatchSequence</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>
