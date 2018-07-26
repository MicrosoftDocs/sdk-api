---
UID: NF:msi.MsiDetermineApplicablePatchesW
title: MsiDetermineApplicablePatchesW function
author: windows-sdk-content
description: The MsiDetermineApplicablePatches function takes a set of patch files, XML files, and XML blobs and determines which patches apply to a specified Windows Installer package and in what sequence.
old-location: setup\msidetermineapplicablepatches.htm
old-project: Msi
ms.assetid: 2362d1dd-695e-48a3-b8ef-4516952ed253
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: MsiDetermineApplicablePatches, MsiDetermineApplicablePatches function, MsiDetermineApplicablePatchesA, MsiDetermineApplicablePatchesW, msi/MsiDetermineApplicablePatches, msi/MsiDetermineApplicablePatchesA, msi/MsiDetermineApplicablePatchesW, setup.msidetermineapplicablepatches
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - MsiDetermineApplicablePatches
 - MsiDetermineApplicablePatchesA
 - MsiDetermineApplicablePatchesW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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

Pointer to an array of <a href="https://msdn.microsoft.com/75f76d85-39f6-4a2c-8b5f-1238639a2014">MSIPATCHSEQUENCEINFO</a> structures. 


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
This error can be returned if the function was called from a <a href="https://msdn.microsoft.com/4a1f3ccc-4904-47d0-bfc6-013e404de47e">custom action</a>  or if MSXML 3.0 is not installed. 

</td>
</tr>
</table>
 




## -remarks



If this function is called from a custom action it fails and returns ERROR_CALL_NOT_IMPLEMENTED.  The function requires MSXML version 3.0 to process XML and returns ERROR_CALL_NOT_IMPLEMENTED if MSXML 3.0 is not installed.


The <b>MsiDetermineApplicablePatches</b> function sets the <b>uStatus</b> and <b>dwOrder</b> members of each <a href="https://msdn.microsoft.com/75f76d85-39f6-4a2c-8b5f-1238639a2014">MSIPATCHSEQUENCEINFO</a> structure pointed to by <i>pPatchInfo</i>. Each structure contains information about a particular patch.

If the function succeeds, the <a href="https://msdn.microsoft.com/75f76d85-39f6-4a2c-8b5f-1238639a2014">MSIPATCHSEQUENCEINFO</a> structure of every patch that can be applied  to the product returns with a  <b>uStatus</b> of ERROR_SUCCESS and a <b>dwOrder</b> greater than or equal to zero. The values of <b>dwOrder</b>  greater than or equal to zero indicate the best application sequence for the patches starting with zero.

If the function succeeds, patches excluded from the best patching sequence return a <a href="https://msdn.microsoft.com/75f76d85-39f6-4a2c-8b5f-1238639a2014">MSIPATCHSEQUENCEINFO</a> structure with a <b>dwOrder</b> equal to -1.  In these cases, a <b>uStatus</b> field of  ERROR_SUCCESS indicates a patch that is  obsolete or superseded for the product.   A <b>uStatus</b> field of ERROR_PATCH_TARGET_NOT_FOUND indicates a patch that is inapplicable to the product.

If the function fails, the <a href="https://msdn.microsoft.com/75f76d85-39f6-4a2c-8b5f-1238639a2014">MSIPATCHSEQUENCEINFO</a> structure for every patch  returns a  <b>dwOrder</b> equal to -1.  In this case, the <b>uStatus</b> fields  can contain errors with more information about individual patches. For example, ERROR_PATCH_NO_SEQUENCE is returned for patches that have circular sequencing information.




## -see-also




<a href="https://msdn.microsoft.com/f82e7d42-f0cd-4d25-b56f-7e423cb64cfd">MsiDeterminePatchSequence</a>



<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="https://msdn.microsoft.com/33cedd37-0343-471c-ad4b-0db5f98d5894">ProductCode</a>
 

 

