---
UID: NS:wincrypt._CRL_INFO
title: CRL_INFO (wincrypt.h)
description: Contains the information of a certificate revocation list (CRL).
helpviewer_keywords: ["*PCRL_INFO","CRL_INFO","CRL_INFO structure [Security]","CRL_V1","CRL_V2","PCRL_INFO","PCRL_INFO structure pointer [Security]","_crypto2_crl_info","security.crl_info","wincrypt/CRL_INFO","wincrypt/PCRL_INFO"]
old-location: security\crl_info.htm
tech.root: security
ms.assetid: 06a28de3-dd7c-4efe-9baa-20aac69d63f3
ms.date: 12/05/2018
ms.keywords: '*PCRL_INFO, CRL_INFO, CRL_INFO structure [Security], CRL_V1, CRL_V2, PCRL_INFO, PCRL_INFO structure pointer [Security], _crypto2_crl_info, security.crl_info, wincrypt/CRL_INFO, wincrypt/PCRL_INFO'
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
req.typenames: CRL_INFO, *PCRL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRL_INFO
 - wincrypt/_CRL_INFO
 - PCRL_INFO
 - wincrypt/PCRL_INFO
 - CRL_INFO
 - wincrypt/CRL_INFO
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
 - CRL_INFO
---

# CRL_INFO structure


## -description

The <b>CRL_INFO</b> structure contains the information of a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).

## -struct-fields

### -field dwVersion

Version number of the CRL. Currently defined version numbers are shown in the following table. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRL_V1"></a><a id="crl_v1"></a><dl>
<dt><b>CRL_V1</b></dt>
</dl>
</td>
<td width="60%">
version 1

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_V2"></a><a id="crl_v2"></a><dl>
<dt><b>CRL_V2</b></dt>
</dl>
</td>
<td width="60%">
version 2

</td>
</tr>
</table>

### -field SignatureAlgorithm

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of a signature algorithm and any associated additional parameters.

### -field Issuer

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> structure that contains an encoded certificate issuer's name.

### -field ThisUpdate

Indication of the date and time of the CRL's published. If the time is after 1950 and before 2050, it is UTC-time encoded as an 8-byte date/time precise to seconds with a 2-digit year (that is, YYMMDDHHMMSS plus 2 bytes). Otherwise, it is generalized-time encoded as an 8-byte year precise to milliseconds with a 4-byte year.

### -field NextUpdate

Indication of the date and time for the CRL's next available scheduled update. If the time is after 1950 and before 2050, it is UTC-time encoded as an 8-byte date/time precise to seconds with a 2-digit year (that is, YYMMDDHHMMSS plus 2 bytes). Otherwise, it is generalized-time encoded as an 8-byte date time precise to milliseconds with a 4-byte year.

### -field cCRLEntry

Number of elements in the <b>rgCRLEntry</b> array.

### -field rgCRLEntry

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_entry">CRL_ENTRY</a> structures. Each of these structures represents a revoked certificate.

### -field cExtension

Number of elements in the <b>rgExtension</b> array.

### -field rgExtension

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures, each holding information about the CRL.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_entry">CRL_ENTRY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycrlrevocation">CertVerifyCRLRevocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignandencodecertificate">CryptSignAndEncodeCertificate</a>