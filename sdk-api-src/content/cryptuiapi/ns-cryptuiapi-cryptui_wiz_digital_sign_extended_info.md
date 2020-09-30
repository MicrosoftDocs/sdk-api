---
UID: NS:cryptuiapi._CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
title: CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO (cryptuiapi.h)
description: Used with the CRYPTUI_WIZ_DIGITAL_SIGN_INFO structure to contain extended information about a signature.
helpviewer_keywords: ["*PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO","CRYPTUI_WIZ_DIGITAL_SIGN_COMMERCIAL","CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO","CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO structure [Security]","CRYPTUI_WIZ_DIGITAL_SIGN_INDIVIDUAL","PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO","PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO structure pointer [Security]","cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO","cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO","security.cryptui_wiz_digital_sign_extended_info"]
old-location: security\cryptui_wiz_digital_sign_extended_info.htm
tech.root: security
ms.assetid: e061aac4-8c9f-4282-a8f8-bc0c5a10e566
ms.date: 12/05/2018
ms.keywords: '*PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_COMMERCIAL, CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO structure [Security], CRYPTUI_WIZ_DIGITAL_SIGN_INDIVIDUAL, PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO structure pointer [Security], cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, security.cryptui_wiz_digital_sign_extended_info'
req.header: cryptuiapi.h
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
req.typenames: CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO, *PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
 - cryptuiapi/_CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
 - PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
 - cryptuiapi/PCRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
 - CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
 - cryptuiapi/CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptuiapi.h
api_name:
 - CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO
---

# CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO structure


## -description

<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_EXTENDED_INFO</b> structure is used with the <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_info">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a> structure to contain extended information about a signature.

## -struct-fields

### -field dwSize

The size, in bytes, of the structure.

### -field dwAttrFlags

A value that indicates the type of the signature. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_COMMERCIAL"></a><a id="cryptui_wiz_digital_sign_commercial"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_COMMERCIAL</b></dt>
</dl>
</td>
<td width="60%">
The signature is a commercial signature.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_DIGITAL_SIGN_INDIVIDUAL"></a><a id="cryptui_wiz_digital_sign_individual"></a><dl>
<dt><b>CRYPTUI_WIZ_DIGITAL_SIGN_INDIVIDUAL</b></dt>
</dl>
</td>
<td width="60%">
The signature is a personal signature.

</td>
</tr>
</table>

### -field pwszDescription

A pointer to a null-terminated Unicode string that contains the description of the subject of the signature.

### -field pwszMoreInfoLocation

A pointer to a null-terminated Unicode string that contains the location from which to get more information about the file. This information will be displayed when the file is downloaded.

### -field pszHashAlg

A pointer to a null-terminated ANSI string that contains the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the hash algorithm used for the signature. The default value is <b>NULL</b>, which indicates that the SHA-1 hash algorithm is used.

### -field pwszSigningCertDisplayString

A pointer to a null-terminated Unicode string that contains the string displayed on the digital signature wizard page. The string should prompt the user to select a certificate for a specific purpose.

### -field hAdditionalCertStore

A handle to an additional certificate store that will be added to the signature.

### -field psAuthenticated

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure that contains authenticated attributes supplied by the user.

### -field psUnauthenticated

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attributes">CRYPT_ATTRIBUTES</a> structure that contains unauthenticated attributes supplied by the user.

## -see-also

<a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_info">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a>