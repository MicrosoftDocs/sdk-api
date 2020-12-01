---
UID: NS:winsafer._SAFER_IDENTIFICATION_HEADER
title: SAFER_IDENTIFICATION_HEADER (winsafer.h)
description: SAFER_IDENTIFICATION_HEADER structure is used as the header for the SAFER_PATHNAME_IDENTIFICATION, SAFER_HASH_IDENTIFICATION, and SAFER_URLZONE_IDENTIFICATION structures.
helpviewer_keywords: ["*PSAFER_IDENTIFICATION_HEADER","PSAFER_IDENTIFICATION_HEADER","PSAFER_IDENTIFICATION_HEADER structure pointer [Security]","SAFER_IDENTIFICATION_HEADER","SAFER_IDENTIFICATION_HEADER structure [Security]","SaferIdentityDefault","SaferIdentityTypeCertificate","SaferIdentityTypeImageHash","SaferIdentityTypeImageName","SaferIdentityTypeUrlZone","_mnp_safer_identification_header","security.safer_identification_header","winsafer/PSAFER_IDENTIFICATION_HEADER","winsafer/SAFER_IDENTIFICATION_HEADER"]
old-location: security\safer_identification_header.htm
tech.root: security
ms.assetid: 9bcb7d22-2360-4146-9972-118ba8822aa7
ms.date: 12/05/2018
ms.keywords: '*PSAFER_IDENTIFICATION_HEADER, PSAFER_IDENTIFICATION_HEADER, PSAFER_IDENTIFICATION_HEADER structure pointer [Security], SAFER_IDENTIFICATION_HEADER, SAFER_IDENTIFICATION_HEADER structure [Security], SaferIdentityDefault, SaferIdentityTypeCertificate, SaferIdentityTypeImageHash, SaferIdentityTypeImageName, SaferIdentityTypeUrlZone, _mnp_safer_identification_header, security.safer_identification_header, winsafer/PSAFER_IDENTIFICATION_HEADER, winsafer/SAFER_IDENTIFICATION_HEADER'
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
req.typenames: SAFER_IDENTIFICATION_HEADER, *PSAFER_IDENTIFICATION_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAFER_IDENTIFICATION_HEADER
 - winsafer/_SAFER_IDENTIFICATION_HEADER
 - PSAFER_IDENTIFICATION_HEADER
 - winsafer/PSAFER_IDENTIFICATION_HEADER
 - SAFER_IDENTIFICATION_HEADER
 - winsafer/SAFER_IDENTIFICATION_HEADER
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
 - SAFER_IDENTIFICATION_HEADER
---

# SAFER_IDENTIFICATION_HEADER structure


## -description

The <b>SAFER_IDENTIFICATION_HEADER</b> structure is used as the header for the  
<a href="/windows/desktop/api/winsafer/ns-winsafer-safer_pathname_identification">SAFER_PATHNAME_IDENTIFICATION</a>, 
<a href="/windows/desktop/api/winsafer/ns-winsafer-safer_hash_identification">SAFER_HASH_IDENTIFICATION</a>, and 
<a href="/windows/desktop/api/winsafer/ns-winsafer-safer_urlzone_identification">SAFER_URLZONE_IDENTIFICATION</a> structures.

## -struct-fields

### -field dwIdentificationType

<a href="/windows/desktop/api/winsafer/ne-winsafer-safer_identification_types">SAFER_IDENTIFICATION_TYPES</a> enumeration value that indicates the type of the structure. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityDefault"></a><a id="saferidentitydefault"></a><a id="SAFERIDENTITYDEFAULT"></a><dl>
<dt><b>SaferIdentityDefault</b></dt>
</dl>
</td>
<td width="60%">
The header is for a default structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityTypeImageName"></a><a id="saferidentitytypeimagename"></a><a id="SAFERIDENTITYTYPEIMAGENAME"></a><dl>
<dt><b>SaferIdentityTypeImageName</b></dt>
</dl>
</td>
<td width="60%">
The header is for a <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_pathname_identification">SAFER_PATHNAME_IDENTIFICATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityTypeImageHash"></a><a id="saferidentitytypeimagehash"></a><a id="SAFERIDENTITYTYPEIMAGEHASH"></a><dl>
<dt><b>SaferIdentityTypeImageHash</b></dt>
</dl>
</td>
<td width="60%">
The header is for a <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_hash_identification">SAFER_HASH_IDENTIFICATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityTypeUrlZone"></a><a id="saferidentitytypeurlzone"></a><a id="SAFERIDENTITYTYPEURLZONE"></a><dl>
<dt><b>SaferIdentityTypeUrlZone</b></dt>
</dl>
</td>
<td width="60%">
The header is for a <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_urlzone_identification">SAFER_URLZONE_IDENTIFICATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SaferIdentityTypeCertificate"></a><a id="saferidentitytypecertificate"></a><a id="SAFERIDENTITYTYPECERTIFICATE"></a><dl>
<dt><b>SaferIdentityTypeCertificate</b></dt>
</dl>
</td>
<td width="60%">
The header is for a <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_pathname_identification">SAFER_PATHNAME_IDENTIFICATION</a> structure.

</td>
</tr>
</table>

### -field cbStructSize

The size of the entire  <a href="/windows/desktop/api/winsafer/ns-winsafer-safer_pathname_identification">SAFER_PATHNAME_IDENTIFICATION</a>, 
<a href="/windows/desktop/api/winsafer/ns-winsafer-safer_hash_identification">SAFER_HASH_IDENTIFICATION</a>, or 
<a href="/windows/desktop/api/winsafer/ns-winsafer-safer_urlzone_identification">SAFER_URLZONE_IDENTIFICATION</a> structure, including the common header.

### -field IdentificationGuid

The GUID of the identification.

### -field lastModified

### -field LastModified

The date and time of the last change to this identification.