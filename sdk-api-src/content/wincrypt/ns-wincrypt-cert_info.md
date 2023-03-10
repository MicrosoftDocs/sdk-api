---
UID: NS:wincrypt._CERT_INFO
title: CERT_INFO (wincrypt.h)
description: Contains the information of a certificate.
helpviewer_keywords: ["*PCERT_INFO","CERT_INFO","CERT_INFO structure [Security]","CERT_V1","CERT_V2","CERT_V3","PCERT_INFO","PCERT_INFO structure pointer [Security]","_crypto2_cert_info","security.cert_info","wincrypt/CERT_INFO","wincrypt/PCERT_INFO"]
old-location: security\cert_info.htm
tech.root: security
ms.assetid: 8d0a3053-52d4-437a-bf55-6724b5825cdc
ms.date: 12/05/2018
ms.keywords: '*PCERT_INFO, CERT_INFO, CERT_INFO structure [Security], CERT_V1, CERT_V2, CERT_V3, PCERT_INFO, PCERT_INFO structure pointer [Security], _crypto2_cert_info, security.cert_info, wincrypt/CERT_INFO, wincrypt/PCERT_INFO'
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
req.typenames: CERT_INFO, *PCERT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_INFO
 - wincrypt/_CERT_INFO
 - PCERT_INFO
 - wincrypt/PCERT_INFO
 - CERT_INFO
 - wincrypt/CERT_INFO
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
 - CERT_INFO
---

# CERT_INFO structure


## -description

The <b>CERT_INFO</b> structure contains the information of a certificate.

## -struct-fields

### -field dwVersion

The version number of a certificate. This member can be one of the following version numbers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_V1"></a><a id="cert_v1"></a><dl>
<dt><b>CERT_V1</b></dt>
</dl>
</td>
<td width="60%">
Version 1

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_V2"></a><a id="cert_v2"></a><dl>
<dt><b>CERT_V2</b></dt>
</dl>
</td>
<td width="60%">
Version 2

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_V3"></a><a id="cert_v3"></a><dl>
<dt><b>CERT_V3</b></dt>
</dl>
</td>
<td width="60%">
Version 3

</td>
</tr>
</table>

### -field SerialNumber

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains the serial number of a certificate. The least significant byte is the zero byte of the <b>pbData</b> member of <i>SerialNumber</i>. The index for the last byte of <b>pbData</b>, is one less than the value of the <b>cbData</b> member of <i>SerialNumber</i>. The most significant byte is the last byte of <b>pbData</b>. Leading 0x00 or 0xFF bytes are removed. For more information, see <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcompareintegerblob">CertCompareIntegerBlob</a>.

### -field SignatureAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature algorithm type and encoded additional encryption parameters.

### -field Issuer

The name, in encoded form, of the issuer of the certificate.

### -field NotBefore

Date and time before which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded Coordinated Universal Time (Greenwich Mean Time) format in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four-digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotBefore</b> time is only precise to seconds.

### -field NotAfter

Date and time after which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded Coordinated Universal Time format in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four-digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotAfter</b> time is only precise to seconds.

### -field Subject

The encoded name of the subject of the certificate.

### -field SubjectPublicKeyInfo

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure that contains the encoded public key and its algorithm. The <b>PublicKey</b> member of the <b>CERT_PUBLIC_KEY_INFO</b> structure contains the encoded public key as a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a>, and the <b>Algorithm</b> member contains the encoded algorithm as a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>.

### -field IssuerUniqueId

A BLOB that contains a unique identifier of the issuer.

### -field SubjectUniqueId

A BLOB that contains a unique identifier of the subject.

### -field cExtension

The number of elements in the <b>rgExtension</b> array.

### -field rgExtension

An array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures, each of which contains extension information about the certificate.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_enveloped_encode_info">CMSG_ENVELOPED_ENCODE_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_encode_info">CMSG_SIGNER_ENCODE_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcomparecertificate">CertCompareCertificate</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore">CertGetSubjectCertificateFromStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgcontrol">CryptMsgControl</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignandencodecertificate">CryptSignAndEncodeCertificate</a>