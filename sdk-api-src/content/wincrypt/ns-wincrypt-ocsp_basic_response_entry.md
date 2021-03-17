---
UID: NS:wincrypt._OCSP_BASIC_RESPONSE_ENTRY
title: OCSP_BASIC_RESPONSE_ENTRY (wincrypt.h)
description: Contains the current certificate status for a single certificate.
helpviewer_keywords: ["*POCSP_BASIC_RESPONSE_ENTRY","OCSP_BASIC_GOOD_CERT_STATUS","OCSP_BASIC_RESPONSE_ENTRY","OCSP_BASIC_RESPONSE_ENTRY structure [Security]","OCSP_BASIC_REVOKED_CERT_STATUS","OCSP_BASIC_UNKNOWN_CERT_STATUS","POCSP_BASIC_RESPONSE_ENTRY","POCSP_BASIC_RESPONSE_ENTRY structure pointer [Security]","security.ocsp_basic_response_entry","wincrypt/OCSP_BASIC_RESPONSE_ENTRY","wincrypt/POCSP_BASIC_RESPONSE_ENTRY"]
old-location: security\ocsp_basic_response_entry.htm
tech.root: security
ms.assetid: c22f25fd-bbee-45de-9ca0-064b159abb7c
ms.date: 12/05/2018
ms.keywords: '*POCSP_BASIC_RESPONSE_ENTRY, OCSP_BASIC_GOOD_CERT_STATUS, OCSP_BASIC_RESPONSE_ENTRY, OCSP_BASIC_RESPONSE_ENTRY structure [Security], OCSP_BASIC_REVOKED_CERT_STATUS, OCSP_BASIC_UNKNOWN_CERT_STATUS, POCSP_BASIC_RESPONSE_ENTRY, POCSP_BASIC_RESPONSE_ENTRY structure pointer [Security], security.ocsp_basic_response_entry, wincrypt/OCSP_BASIC_RESPONSE_ENTRY, wincrypt/POCSP_BASIC_RESPONSE_ENTRY'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: OCSP_BASIC_RESPONSE_ENTRY, *POCSP_BASIC_RESPONSE_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_BASIC_RESPONSE_ENTRY
 - wincrypt/_OCSP_BASIC_RESPONSE_ENTRY
 - POCSP_BASIC_RESPONSE_ENTRY
 - wincrypt/POCSP_BASIC_RESPONSE_ENTRY
 - OCSP_BASIC_RESPONSE_ENTRY
 - wincrypt/OCSP_BASIC_RESPONSE_ENTRY
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
 - OCSP_BASIC_RESPONSE_ENTRY
---

# OCSP_BASIC_RESPONSE_ENTRY structure


## -description

The <b>OCSP_BASIC_RESPONSE_ENTRY</b> structure contains the current certificate status for a single certificate. This structure populates the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_info">OCSP_BASIC_RESPONSE_INFO</a> <b>rgResponseEntry</b> member.

## -struct-fields

### -field CertId

An <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_cert_id">OCSP_CERT_ID</a> structure that specifies the target certificate of the <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) response.

### -field dwCertStatus

A value that indicates the target certificate revocation status.


<a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560</a> defines the following possible values for certificate status.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OCSP_BASIC_GOOD_CERT_STATUS"></a><a id="ocsp_basic_good_cert_status"></a><dl>
<dt><b>OCSP_BASIC_GOOD_CERT_STATUS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The certificate is not revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_BASIC_REVOKED_CERT_STATUS"></a><a id="ocsp_basic_revoked_cert_status"></a><dl>
<dt><b>OCSP_BASIC_REVOKED_CERT_STATUS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The certificate is revoked either permanently or temporarily.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_BASIC_UNKNOWN_CERT_STATUS"></a><a id="ocsp_basic_unknown_cert_status"></a><dl>
<dt><b>OCSP_BASIC_UNKNOWN_CERT_STATUS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The responder has no information for the target certificate.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.pRevokedInfo

A pointer to an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_revoked_info">OCSP_BASIC_REVOKED_INFO</a> structure that specifies the reason the target certificate was revoked.

### -field ThisUpdate

The date and time at which the response indicated by <i>dwCertStatus</i> is known to be correct.

### -field NextUpdate

The date and time on or before which newer information will be available for the certificate status. A value of zero indicates that the certificate status never expires.

### -field cExtension

The number of elements in the <b>rgExtension</b> array.

### -field rgExtension

An array of pointers to  <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures, each of which contains additional information about the response.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_info">OCSP_BASIC_RESPONSE_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_revoked_info">OCSP_BASIC_REVOKED_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_cert_id">OCSP_CERT_ID</a>



<a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560 Online Certificate Status Protocol</a>