---
UID: NS:winsafer._SAFER_CODE_PROPERTIES_V2
title: SAFER_CODE_PROPERTIES_V2 (winsafer.h)
description: Contains code image information and criteria to be checked on the code image.S
helpviewer_keywords: ["*PSAFER_CODE_PROPERTIES","*PSAFER_CODE_PROPERTIES_V2","PSAFER_CODE_PROPERTIES","PSAFER_CODE_PROPERTIES structure pointer [Security]","SAFER_CODE_PROPERTIES","SAFER_CODE_PROPERTIES  [Security] See also","SAFER_CODE_PROPERTIES_V1  [Security]","SAFER_CODE_PROPERTIES [Security]","SAFER_CODE_PROPERTIES structure [Security]","SAFER_CODE_PROPERTIES_V2","SAFER_CODE_PROPERTIES_V2  [Security] See","SAFER_CODE_PROPERTIES  [Security]","SAFER_CRITERIA_APPX_PACKAGE","SAFER_CRITERIA_AUTHENTICODE","SAFER_CRITERIA_IMAGEHASH","SAFER_CRITERIA_IMAGEPATH","SAFER_CRITERIA_IMAGEPATH_NT","SAFER_CRITERIA_URLZONE","_mnp_safer_code_properties","security.safer_code_properties","winsafer/PSAFER_CODE_PROPERTIES","winsafer/SAFER_CODE_PROPERTIES"]
old-location: security\safer_code_properties.htm
tech.root: security
ms.assetid: 039a37a9-1744-4cff-919e-e0da50d7b291
ms.date: 12/05/2018
ms.keywords: '*PSAFER_CODE_PROPERTIES, *PSAFER_CODE_PROPERTIES_V2, PSAFER_CODE_PROPERTIES, PSAFER_CODE_PROPERTIES structure pointer [Security], SAFER_CODE_PROPERTIES, SAFER_CODE_PROPERTIES  [Security] See also,SAFER_CODE_PROPERTIES_V1  [Security], SAFER_CODE_PROPERTIES [Security], SAFER_CODE_PROPERTIES structure [Security], SAFER_CODE_PROPERTIES_V2, SAFER_CODE_PROPERTIES_V2  [Security] See ,SAFER_CODE_PROPERTIES  [Security], SAFER_CRITERIA_APPX_PACKAGE, SAFER_CRITERIA_AUTHENTICODE, SAFER_CRITERIA_IMAGEHASH, SAFER_CRITERIA_IMAGEPATH, SAFER_CRITERIA_IMAGEPATH_NT, SAFER_CRITERIA_URLZONE, _mnp_safer_code_properties, security.safer_code_properties, winsafer/PSAFER_CODE_PROPERTIES, winsafer/SAFER_CODE_PROPERTIES'
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SAFER_CODE_PROPERTIES_V2, *PSAFER_CODE_PROPERTIES_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAFER_CODE_PROPERTIES_V2
 - winsafer/_SAFER_CODE_PROPERTIES_V2
 - PSAFER_CODE_PROPERTIES_V2
 - winsafer/PSAFER_CODE_PROPERTIES_V2
 - SAFER_CODE_PROPERTIES_V2
 - winsafer/SAFER_CODE_PROPERTIES_V2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_CODE_PROPERTIES
---

# SAFER_CODE_PROPERTIES_V2 structure


## -description

The <b>SAFER_CODE_PROPERTIES</b> structure contains code image information and criteria to be checked on the code image. An array of <b>SAFER_CODE_PROPERTIES</b> structures is passed to the 
<a href="/windows/desktop/api/winsafer/nf-winsafer-saferidentifylevel">SaferIdentifyLevel</a> function.
			
		

SAFER_CODE_PROPERTIES_V2 is a redefinition of <b>SAFER_CODE_PROPERTIES</b> and is an extended version of <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_code_properties_v1">SAFER_CODE_PROPERTIES_V1</a> because it includes new members for Windows Store app packages. Existing binary callers can distinguish which version by checking the <b>cbSize</b> member.

## -struct-fields

### -field cbSize

The size of this structure in bytes. This is used for future and backward compatibility.

### -field dwCheckFlags

The types of criteria considered when evaluating this structure. Some flags might be silently ignored if some or all of their associated structure elements are not supplied. Specifying zero for this parameter causes the entire structure's contents to be ignored. 




The following table shows the possible values. These values may be combined using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SAFER_CRITERIA_IMAGEPATH"></a><a id="safer_criteria_imagepath"></a><dl>
<dt><b>SAFER_CRITERIA_IMAGEPATH</b></dt>
<dt>0x00001</dt>
</dl>
</td>
<td width="60%">
Check the code image path.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_CRITERIA_IMAGEHASH"></a><a id="safer_criteria_imagehash"></a><dl>
<dt><b>SAFER_CRITERIA_IMAGEHASH</b></dt>
<dt>0x00004</dt>
</dl>
</td>
<td width="60%">
Check the code hash.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_CRITERIA_AUTHENTICODE"></a><a id="safer_criteria_authenticode"></a><dl>
<dt><b>SAFER_CRITERIA_AUTHENTICODE</b></dt>
<dt>0x00008</dt>
</dl>
</td>
<td width="60%">
Check the Authenticode signature. If this value is used, either the <b>hImageFileHandle</b> member or the <b>ImagePath</b> member must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_CRITERIA_URLZONE"></a><a id="safer_criteria_urlzone"></a><dl>
<dt><b>SAFER_CRITERIA_URLZONE</b></dt>
<dt>0x00010</dt>
</dl>
</td>
<td width="60%">
Check the URL of origin.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_CRITERIA_IMAGEPATH_NT"></a><a id="safer_criteria_imagepath_nt"></a><dl>
<dt><b>SAFER_CRITERIA_IMAGEPATH_NT</b></dt>
<dt>0x01000</dt>
</dl>
</td>
<td width="60%">
Check the Windows NT image path.

</td>
</tr>
<tr>
<td width="40%"><a id="SAFER_CRITERIA_APPX_PACKAGE"></a><a id="safer_criteria_appx_package"></a><dl>
<dt><b>SAFER_CRITERIA_APPX_PACKAGE</b></dt>
<dt>0x00020</dt>
</dl>
</td>
<td width="60%">
Check for a Windows Store app package. For use by Windows Store apps.

</td>
</tr>
</table>

### -field ImagePath

A string specifying the fully qualified path and file name to be used for discrimination checks based on the path. The image path is also used to open and read the file to identify any other discrimination criteria not supplied in this structure. This member can be <b>NULL</b>; however, if the <b>dwCheckFlags</b> member includes <b>SAFER_CRITERIA_AUTHENTICODE</b>, either this member or the <b>hImageFileHandle</b> member must be set.

### -field hImageFileHandle

A file handle to a code image with at least GENERIC_READ access. The handle is used instead of explicitly reopening the file  to compute discrimination criteria not supplied in this structure. This member can be <b>NULL</b>; however, if <b>dwCheckFlags</b> includes <b>SAFER_CRITERIA_AUTHENTICODE</b>, either this member or the <b>ImagePath</b> member must be set.

### -field UrlZoneId

The predetermined Internet Explorer security zones. The following zones are defined: 




<ul>
<li>URLZONE_LOCAL_MACHINE</li>
<li>URLZONE_INTRANET</li>
<li>URLZONE_TRUSTED</li>
<li>URLZONE_INTERNET</li>
<li>URLZONE_UNTRUSTED</li>
</ul>
This member can be set to 0.

### -field ImageHash

The pre-computed hash of the image. The supplied hash is interpreted as  valid if both the <b>ImageSize</b> member and the <b>dwImageHashSize</b> member are nonzero and the <b>HashAlgorithm</b> member contains a valid hashing algorithm from Wincrypt.h. 




If the supplied hash fails to meet these conditions, the hash will be automatically recomputed  by:

<ul>
<li>Using the <b>ImageSize</b> member and the <b>pByteBlock</b> member if both are nonzero.</li>
<li>Using the <b>hImageFileHandle</b> member if it is not <b>NULL</b>.</li>
<li>Opening and using the <b>ImagePath</b> member if it is not <b>NULL</b>.</li>
</ul>

### -field dwImageHashSize

The size in bytes of the <b>ImageHash</b> member.

### -field ImageSize

The size in bytes of the <b>pByteBlock</b> member. This member is not used if the <b>pByteBlock</b> member is <b>NULL</b>.

### -field HashAlgorithm

The hash algorithm used to create the <b>ImageHash</b> member.

### -field pByteBlock

The memory block containing the image of the code being checked. This member is optional. If this member is specified, the <b>ImageSize</b> member must also be supplied.

### -field hWndParent

The arguments used for Authenticode signer certificate verification. These arguments are passed to the <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> function and control the user interface (UI) that prompts the user to accept or reject entrusted certificates.

### -field dwWVTUIChoice

Indicates  the type of UI used. The following table shows the possible values. 
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WTD_UI_ALL</dt>
</dl>
</td>
<td width="60%">
Display all UI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WTD_UI_NONE</dt>
</dl>
</td>
<td width="60%">
Display no UI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WTD_UI_NOBAD</dt>
</dl>
</td>
<td width="60%">
Display UI only if there were no errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>WTD_UI_NOGOOD</dt>
</dl>
</td>
<td width="60%">
Display UI only if an error occurs.

</td>
</tr>
</table>

### -field PackageMoniker

The package moniker property. For use by Windows Store apps.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available.

### -field PackagePublisher

The package publisher property. For use by Windows Store apps.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available.

### -field PackageName

The package name property. For use by Windows Store apps.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available.

### -field PackageVersion

The package version property. For use by Windows Store apps.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available.

### -field PackageIsFramework

The package is a framework package. For use by Windows Store apps.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available.
