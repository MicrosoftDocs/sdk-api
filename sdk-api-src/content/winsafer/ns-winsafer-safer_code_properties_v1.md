---
UID: NS:winsafer._SAFER_CODE_PROPERTIES_V1
title: SAFER_CODE_PROPERTIES_V1 (winsafer.h)
description: Contains code image information and criteria to be checked on the code image. (SAFER_CODE_PROPERTIES_V1)
helpviewer_keywords: ["*PSAFER_CODE_PROPERTIES_V1","PSAFER_CODE_PROPERTIES_V1","PSAFER_CODE_PROPERTIES_V1 structure pointer [Security]","SAFER_CODE_PROPERTIES_V1","SAFER_CODE_PROPERTIES_V1  [Security] See also","SAFER_CODE_PROPERTIES  [Security]","SAFER_CODE_PROPERTIES_V1 [Security]","SAFER_CODE_PROPERTIES_V1 structure [Security]","SAFER_CRITERIA_AUTHENTICODE","SAFER_CRITERIA_IMAGEHASH","SAFER_CRITERIA_IMAGEPATH","SAFER_CRITERIA_IMAGEPATH_NT","SAFER_CRITERIA_URLZONE","security.safer_code_properties_v1","winsafer/PSAFER_CODE_PROPERTIES_V1","winsafer/SAFER_CODE_PROPERTIES_V1"]
old-location: security\safer_code_properties_v1.htm
tech.root: security
ms.assetid: E09D287B-7223-4CAF-B404-61FB6871B622
ms.date: 12/05/2018
ms.keywords: '*PSAFER_CODE_PROPERTIES_V1, PSAFER_CODE_PROPERTIES_V1, PSAFER_CODE_PROPERTIES_V1 structure pointer [Security], SAFER_CODE_PROPERTIES_V1, SAFER_CODE_PROPERTIES_V1  [Security] See also,SAFER_CODE_PROPERTIES  [Security], SAFER_CODE_PROPERTIES_V1 [Security], SAFER_CODE_PROPERTIES_V1 structure [Security], SAFER_CRITERIA_AUTHENTICODE, SAFER_CRITERIA_IMAGEHASH, SAFER_CRITERIA_IMAGEPATH, SAFER_CRITERIA_IMAGEPATH_NT, SAFER_CRITERIA_URLZONE, security.safer_code_properties_v1, winsafer/PSAFER_CODE_PROPERTIES_V1, winsafer/SAFER_CODE_PROPERTIES_V1'
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
req.typenames: SAFER_CODE_PROPERTIES_V1, *PSAFER_CODE_PROPERTIES_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAFER_CODE_PROPERTIES_V1
 - winsafer/_SAFER_CODE_PROPERTIES_V1
 - PSAFER_CODE_PROPERTIES_V1
 - winsafer/PSAFER_CODE_PROPERTIES_V1
 - SAFER_CODE_PROPERTIES_V1
 - winsafer/SAFER_CODE_PROPERTIES_V1
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
 - SAFER_CODE_PROPERTIES_V1
---

# SAFER_CODE_PROPERTIES_V1 structure


## -description

The <b>SAFER_CODE_PROPERTIES_V1</b> structure contains code image information and criteria to be checked on the code image. An array of <b>SAFER_CODE_PROPERTIES_V1</b> structures is passed to the 
<a href="/windows/desktop/api/winsafer/nf-winsafer-saferidentifylevel">SaferIdentifyLevel</a> function.
			
		
			
		

SAFER_CODE_PROPERTIES_V1 does not include the new members for Windows Store app packages. Existing binary callers can distinguish which version by checking the <b>cbSize</b> member.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure. This is used for future and backward compatibility.

### -field dwCheckFlags

The types of criteria considered when evaluating this structure. Some flags might be silently ignored if some or all of their associated structure elements are not supplied. Specifying zero for this parameter causes the entire structure's contents to be ignored. 




The following table shows the possible values. These values can be combined by using a bitwise-<b>OR</b> operation.

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
</table>

### -field ImagePath

A string that specifies the fully qualified path and file name to be used for discrimination checks based on the path. The image path is also used to open and read the file to identify any other discrimination criteria not supplied in this structure. This member can be <b>NULL</b>; however, if the <b>dwCheckFlags</b> member includes <b>SAFER_CRITERIA_AUTHENTICODE</b>, either this member or the <b>hImageFileHandle</b> member must be set.

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

The precomputed hash of the image. The supplied hash is interpreted as  valid if both the <b>ImageSize</b> member and the <b>dwImageHashSize</b> member are nonzero and the <b>HashAlgorithm</b> member contains a valid hashing algorithm from Wincrypt.h. 




If the supplied hash fails to meet these conditions, the hash is automatically recomputed  by:

<ul>
<li>Using the <b>ImageSize</b> member and the <b>pByteBlock</b> member, if both are nonzero.</li>
<li>Using the <b>hImageFileHandle</b> member, if it is not <b>NULL</b>.</li>
<li>Opening and using the <b>ImagePath</b> member, if it is not <b>NULL</b>.</li>
</ul>

### -field dwImageHashSize

The size, in bytes, of the <b>ImageHash</b> member.

### -field ImageSize

The size, in bytes, of the <b>pByteBlock</b> member. This member is not used if the <b>pByteBlock</b> member is <b>NULL</b>.

### -field HashAlgorithm

The hash algorithm used to create the <b>ImageHash</b> member.

### -field pByteBlock

The memory block that contains the image of the code being checked. This member is optional. If this member is specified, the <b>ImageSize</b> member must also be supplied.

### -field hWndParent

The arguments used for Authenticode signer certificate verification. These arguments are passed to the <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> function and control the UI that prompts the user to accept or reject entrusted certificates.

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

## -remarks

<a href="/windows/desktop/api/winsafer/ns-winsafer-safer_code_properties_v2">SAFER_CODE_PROPERTIES</a>  was redefined to include additional members that allow Windows Store app to use the structure. Check the <b>cbSize</b> member for the appropriate size of the structure and for whether you should use the <b>SAFER_CODE_PROPERTIES</b> structure or the <b>SAFER_CODE_PROPERTIES_V1</b> structure.
