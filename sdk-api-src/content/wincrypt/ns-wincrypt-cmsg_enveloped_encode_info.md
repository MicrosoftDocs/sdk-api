---
UID: NS:wincrypt._CMSG_ENVELOPED_ENCODE_INFO
title: CMSG_ENVELOPED_ENCODE_INFO (wincrypt.h)
description: Contains information needed to encode an enveloped message. It is passed to CryptMsgOpenToEncode if the dwMsgType parameter is CMSG_ENVELOPED.
helpviewer_keywords: ["*PCMSG_ENVELOPED_ENCODE_INFO","All other encryption algorithms","CALG_3DES","CALG_DES","CMSG_ENVELOPED_ENCODE_INFO","CMSG_ENVELOPED_ENCODE_INFO structure [Security]","PCMSG_ENVELOPED_ENCODE_INFO","PCMSG_ENVELOPED_ENCODE_INFO structure pointer [Security]","RC2","RC4","SP3 or compatible","_crypto2_cmsg_enveloped_encode_info","security.cmsg_enveloped_encode_info","wincrypt/CMSG_ENVELOPED_ENCODE_INFO","wincrypt/PCMSG_ENVELOPED_ENCODE_INFO"]
old-location: security\cmsg_enveloped_encode_info.htm
tech.root: security
ms.assetid: 87712541-2806-4709-a7cf-c9ba966c96fd
ms.date: 12/05/2018
ms.keywords: '*PCMSG_ENVELOPED_ENCODE_INFO, All other encryption algorithms, CALG_3DES, CALG_DES, CMSG_ENVELOPED_ENCODE_INFO, CMSG_ENVELOPED_ENCODE_INFO structure [Security], PCMSG_ENVELOPED_ENCODE_INFO, PCMSG_ENVELOPED_ENCODE_INFO structure pointer [Security], RC2, RC4, SP3 or compatible, _crypto2_cmsg_enveloped_encode_info, security.cmsg_enveloped_encode_info, wincrypt/CMSG_ENVELOPED_ENCODE_INFO, wincrypt/PCMSG_ENVELOPED_ENCODE_INFO'
req.header: wincrypt.h
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
req.typenames: CMSG_ENVELOPED_ENCODE_INFO, *PCMSG_ENVELOPED_ENCODE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMSG_ENVELOPED_ENCODE_INFO
 - wincrypt/_CMSG_ENVELOPED_ENCODE_INFO
 - PCMSG_ENVELOPED_ENCODE_INFO
 - wincrypt/PCMSG_ENVELOPED_ENCODE_INFO
 - CMSG_ENVELOPED_ENCODE_INFO
 - wincrypt/CMSG_ENVELOPED_ENCODE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMSG_ENVELOPED_ENCODE_INFO
---

# CMSG_ENVELOPED_ENCODE_INFO structure


## -description

The <b>CMSG_ENVELOPED_ENCODE_INFO</b> structure contains information needed to encode an enveloped message. It is passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a> if the <i>dwMsgType</i> parameter is CMSG_ENVELOPED.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hCryptProv

This member is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>Specifies a handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) used to do content encryption, recipient key encryption, and export. The private keys of the <b>hCryptProv</b> are not used. 


This member's data type is <b>HCRYPTPROV</b>.

Unless there is a strong reason for passing in a specific cryptographic provider in <b>hCryptProv</b>, pass zero to use the default RSA or DSS provider.

### -field ContentEncryptionAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature algorithm type and any associated additional parameters in encoded form. 




The <b>pszObjId</b> member of the structure specifies the algorithm used to encrypt the message contents.

The following encryption algorithms require an encoded eight byte <a href="/windows/desktop/SecGloss/i-gly">initialization vector</a> (IV) in the <b>Parameters</b> member of structure. For details, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CALG_DES"></a><a id="calg_des"></a><dl>
<dt><b>CALG_DES</b></dt>
</dl>
</td>
<td width="60%">
szOID_OIWSEC_desCBC

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_3DES"></a><a id="calg_3des"></a><dl>
<dt><b>CALG_3DES</b></dt>
</dl>
</td>
<td width="60%">
szOID_RSA_DES_EDE3_CBC

</td>
</tr>
</table>
 

If the <b>cbData</b> member of the <b>Parameters</b> member is zero, an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoded OCTET STRING containing the IV is generated using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom">CryptGenRandom</a>.

The szOID_RSA_RC2CBC (CALG_RC2) algorithm requires the <b>pbData</b> member of <b>Parameters</b> to be an encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_rc2_cbc_parameters">CRYPT_RC2_CBC_PARAMETERS</a> structure. If the <b>cbData</b> member of the <b>Parameters</b> member is zero, an ASN.1 encoded CRYPT_RC2_CBC_PARAMETERS is generated with a default value of 40 for the <b>dwVersion</b> member. This sets the default key length to 40 bits. This default key length can be overridden with <b>pvEncryptionAuxInfo</b> pointing to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc2_aux_info">CMSG_RC2_AUX_INFO</a> structure containing the desired key length.

<div class="alert"><b>Note</b>  On decryption, if an IV exists, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a> is called with the IV before decryption begins.</div>
<div> </div>

### -field pvEncryptionAuxInfo

A pointer to a structure depending on the encryption algorithm. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RC2"></a><a id="rc2"></a><dl>
<dt><b>RC2</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc2_aux_info">CMSG_RC2_AUX_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="RC4"></a><a id="rc4"></a><dl>
<dt><b>RC4</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_rc4_aux_info">CMSG_RC4_AUX_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="SP3_or_compatible"></a><a id="sp3_or_compatible"></a><a id="SP3_OR_COMPATIBLE"></a><dl>
<dt><b>SP3 or compatible</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_sp3_compatible_aux_info">CMSG_SP3_COMPATIBLE_AUX_INFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="All_other_encryption_algorithms"></a><a id="all_other_encryption_algorithms"></a><a id="ALL_OTHER_ENCRYPTION_ALGORITHMS"></a><dl>
<dt><b>All other encryption algorithms</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b>

</td>
</tr>
</table>

### -field cRecipients

Number of elements in the <b>rgpRecipients</b> or <b>rgCmsRecipients</b> array.

### -field rgpRecipients

An array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structures, each containing a recipient's certificate Issuer, SerialNumber, and SubjectPublicKeyInfo. This array can only be used for recipients identified by their Issuer and serial number. If <b>rgpRecipients</b> is not <b>NULL</b>, <b>rgCmsRecipients</b> must be <b>NULL</b>.

### -field rgCmsRecipients

Optional. An array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_recipient_encode_info">CMSG_RECIPIENT_ENCODE_INFO</a> structures containing recipient information. If <b>rgCmsRecipients</b> is not <b>NULL</b>, <b>rgpRecipients</b> must be <b>NULL</b>. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.

### -field cCertEncoded

Optional. A <b>DWORD</b> value that indicates the number of encoded certificates in the <b>rgCertEncoded</b> array. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.

### -field rgCertEncoded

Optional. Array of <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_BLOB</a> structures. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.

### -field cCrlEncoded

Optional. A <b>DWORD</b> value that indicates the number of encoded <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) in the <b>rgCRLEncoded</b> array. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.

### -field rgCrlEncoded

Optional. An array of <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRL_BLOB</a> structures. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.

### -field cAttrCertEncoded

Optional. A <b>DWORD</b> value that indicates the number of encoded certificate attributes in the <b>rgAttrCertEncoded</b> array. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.

### -field rgAttrCertEncoded

Optional. An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this member.

### -field cUnprotectedAttr

Optional. A <b>DWORD</b> value that indicates the number of unprotected attributes in the <b>rgUnprotectedAttr</b> array. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.

### -field rgUnprotectedAttr

Optional. An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures. CMSG_ENVELOPED_ENCODE_INFO_HAS_CMS_FIELDS must be defined to reference this field.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>