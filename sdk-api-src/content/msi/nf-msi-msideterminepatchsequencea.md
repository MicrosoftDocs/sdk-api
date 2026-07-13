---
UID: NF:msi.MsiDeterminePatchSequenceA
title: MsiDeterminePatchSequenceA function (msi.h)
description: Takes a set of patch files, XML files, and XML blobs and determines the best sequence of application for the patches to a specified installed product. (ANSI)
helpviewer_keywords: ["MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiDeterminePatchSequenceA", "msi/MsiDeterminePatchSequenceA"]
old-location: setup\msideterminepatchsequence.htm
tech.root: setup
ms.assetid: f82e7d42-f0cd-4d25-b56f-7e423cb64cfd
ms.date: 12/05/2018
ms.keywords: MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiDeterminePatchSequence, MsiDeterminePatchSequence function, MsiDeterminePatchSequenceA, MsiDeterminePatchSequenceW, msi/MsiDeterminePatchSequence, msi/MsiDeterminePatchSequenceA, msi/MsiDeterminePatchSequenceW, setup.msideterminepatchsequence
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDeterminePatchSequenceW (Unicode) and MsiDeterminePatchSequenceA (ANSI)
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
 - MsiDeterminePatchSequenceA
 - msi/MsiDeterminePatchSequenceA
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
 - MsiDeterminePatchSequence
 - MsiDeterminePatchSequenceA
 - MsiDeterminePatchSequenceW
---

# MsiDeterminePatchSequenceA function


## -description

The <b>MsiDeterminePatchSequence</b> function takes a set of patch files, XML files, and XML blobs and determines the best sequence of application for the  patches to a specified installed product. This function accounts for patches that have already been applied to the product and accounts for obsolete and superseded patches.

## -parameters

### -param szProductCode [in]

The product that is the target for the set of patches. The value must be the <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID for the product.

### -param szUserSid [in, optional]

Null-terminated string  that specifies  a security identifier (SID) of a user. This parameter restricts the context of enumeration for  this user account. This parameter cannot be   the special SID strings "S-1-1-0" (everyone) or "S-1-5-18" (local system). For the machine context <i>dwContext</i> is set to<b> MSIINSTALLCONTEXT_MACHINE</b> and <i>szUserSid</i> must be <b>NULL</b>. 
For the current user context <i>szUserSid</i> can be null and  <i>dwContext</i> can be set to <b>MSIINSTALLCONTEXT_USERMANAGED</b> or <b>MSIINSTALLCONTEXT_USERUNMANAGED</b>.

### -param dwContext [in]

Restricts the  enumeration to a per-user-unmanaged,  per-user-managed, or per-machine context. This parameter can be any one of the  following values.

<table>
<tr>
<th>Type of context</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Patches are considered for all per-user-managed installations of the product for  the user specified by <i>szUserSid</i>. A null <i>szUserSid</i> with this context means the current user.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Patches are considered for all per-user-unmanaged installations for the user specified by <i>szUserSid</i>. A null <i>szUserSid</i> with this context means the current user.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Patches are considered for the per-machine installation. When <i>dwContext</i> is set to <b>MSIINSTALLCONTEXT_MACHINE</b>  the <i>szUserSid</i> parameter must be null.

</td>
</tr>
</table>

### -param cPatchInfo [in]

The number of patches in the array.

### -param pPatchInfo [in]

Pointer to an array of <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structures.

## -returns

The <b>MsiDeterminePatchSequence</b> function returns the following values.

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
<dt><b>ERROR_INSTALL_PACKAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The installation package was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
A user that is not an administrator attempted to call the function with a context of a different user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data for a registered patch or product is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID specified is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_NOT_CALLED</b></dt>
</dl>
</td>
<td width="60%">
Windows Installer version 3.0 is required to determine the best patch sequence. The function was called with <i>szProductCode</i> not yet installed with  Windows Installer version 3.0.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PATCH</b></dt>
</dl>
</td>
<td width="60%">
The specified patch is unknown.

</td>
</tr>
</table>

## -remarks

Users that do not have administrator privileges  can call this function only in their own or machine context. Users that are administrators can call it for other users.

If this function is called from a custom action it fails and returns <b>ERROR_CALL_NOT_IMPLEMENTED</b>. The function requires MSXML version 3.0 to process XML and returns <b>ERROR_CALL_NOT_IMPLEMENTED</b> if MSXML 3.0 is not installed.


The <b>MsiDeterminePatchSequence</b> function sets the <b>uStatus</b> and <b>dwOrder</b> members of each <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structure pointed to by <i>pPatchInfo</i>. Each structure contains information about a particular patch.

If the function succeeds, the <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structure of every patch that can be applied  to the product returns with a  <b>uStatus</b> of <b>ERROR_SUCCESS</b> and a <b>dwOrder</b> greater than or equal to zero. The values of <b>dwOrder</b>  greater than or equal to zero indicate the best application sequence for the patches starting with zero.

If the function succeeds, patches excluded from the best patching sequence return a <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structure with a <b>dwOrder</b> equal to -1.  In these cases, a <b>uStatus</b> field of  <b>ERROR_SUCCESS</b> indicates a patch that is  obsolete or superseded for the product.   A <b>uStatus</b> field of <b>ERROR_PATCH_TARGET_NOT_FOUND</b> indicates a patch that is inapplicable to the product.

If the function fails, the <a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a> structure for every patch  returns a  <b>dwOrder</b> equal to -1.  In this case, the <b>uStatus</b> fields  can contain errors with more information about individual patches. For example, <b>ERROR_PATCH_NO_SEQUENCE</b> is returned for patches that have circular sequencing information.





> [!NOTE]
> The msi.h header defines MsiDeterminePatchSequence as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/msi/ns-msi-msipatchsequenceinfoa">MSIPATCHSEQUENCEINFO</a>



<a href="/windows/desktop/api/msi/nf-msi-msidetermineapplicablepatchesa">MsiDetermineApplicablePatches</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>
