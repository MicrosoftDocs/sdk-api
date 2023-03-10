---
UID: NS:wincrypt._CERT_REVOCATION_STATUS
title: CERT_REVOCATION_STATUS (wincrypt.h)
description: Contains information on the revocation status of the certificate.
helpviewer_keywords: ["*PCERT_REVOCATION_STATUS","CERT_REVOCATION_STATUS","CERT_REVOCATION_STATUS structure [Security]","CRL_REASON_AFFILIATION_CHANGED","CRL_REASON_CA_COMPROMISE","CRL_REASON_CERTIFICATE_HOLD","CRL_REASON_CESSATION_OF_OPERATION","CRL_REASON_KEY_COMPROMISE","CRL_REASON_SUPERSEDED","CRL_REASON_UNSPECIFIED","PCERT_REVOCATION_STATUS","PCERT_REVOCATION_STATUS structure pointer [Security]","_crypto2_cert_revocation_status","security.cert_revocation_status","wincrypt/CERT_REVOCATION_STATUS","wincrypt/PCERT_REVOCATION_STATUS"]
old-location: security\cert_revocation_status.htm
tech.root: security
ms.assetid: 087ea37a-907a-4652-a5df-dd8e86755490
ms.date: 12/05/2018
ms.keywords: '*PCERT_REVOCATION_STATUS, CERT_REVOCATION_STATUS, CERT_REVOCATION_STATUS structure [Security], CRL_REASON_AFFILIATION_CHANGED, CRL_REASON_CA_COMPROMISE, CRL_REASON_CERTIFICATE_HOLD, CRL_REASON_CESSATION_OF_OPERATION, CRL_REASON_KEY_COMPROMISE, CRL_REASON_SUPERSEDED, CRL_REASON_UNSPECIFIED, PCERT_REVOCATION_STATUS, PCERT_REVOCATION_STATUS structure pointer [Security], _crypto2_cert_revocation_status, security.cert_revocation_status, wincrypt/CERT_REVOCATION_STATUS, wincrypt/PCERT_REVOCATION_STATUS'
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
req.typenames: CERT_REVOCATION_STATUS, *PCERT_REVOCATION_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_REVOCATION_STATUS
 - wincrypt/_CERT_REVOCATION_STATUS
 - PCERT_REVOCATION_STATUS
 - wincrypt/PCERT_REVOCATION_STATUS
 - CERT_REVOCATION_STATUS
 - wincrypt/CERT_REVOCATION_STATUS
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
 - CERT_REVOCATION_STATUS
---

# CERT_REVOCATION_STATUS structure


## -description

The <b>CERT_REVOCATION_STATUS</b> structure contains information on the revocation status of the certificate. It is passed to and returned by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a>. On return from the function, it specifies the status of a revoked or unchecked context.

## -struct-fields

### -field cbSize

Size of this structure in bytes. 




Upon input to 
<b>CERT_REVOCATION_STATUS</b>, <b>cbSize</b> must be set to a size greater than or equal to the size of a <b>CERT_REVOCATION_STATUS</b> structure. Otherwise, <b>CERT_REVOCATION_STATUS</b> returns <b>FALSE</b> and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns E_INVALIDARG.

### -field dwIndex

Specifies an index value for the <i>rgpvContext</i> array passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a>. It is the index of the first <a href="/windows/desktop/SecGloss/c-gly">context</a> in that array that was revoked or that could not be checked for revocation. For information about the contexts that were not checked, <b>CertVerifyRevocation</b> is called again, specifying a <i>rgpvContext</i> array that contains the unchecked contexts from the original list.

### -field dwError

Specifies the returned error status. This value matches the return value of <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> on return from the call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a>. For the list of these error values, see the table in the Return Values section of 
<b>CertVerifyRevocation</b>.

### -field dwReason

Specifies the cause of the error. This member is set only if <b>dwError</b> is CRYPT_E_REVOKED. It contains a code that indicates why the <a href="/windows/desktop/SecGloss/c-gly">context</a> was revoked. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_UNSPECIFIED"></a><a id="crl_reason_unspecified"></a><dl>
<dt><b>CRL_REASON_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
No reason was specified for revocation.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_KEY_COMPROMISE"></a><a id="crl_reason_key_compromise"></a><dl>
<dt><b>CRL_REASON_KEY_COMPROMISE</b></dt>
</dl>
</td>
<td width="60%">
It is known or suspected that the subject's private key or other aspects of the subject validated in the certificate are compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_CA_COMPROMISE"></a><a id="crl_reason_ca_compromise"></a><dl>
<dt><b>CRL_REASON_CA_COMPROMISE</b></dt>
</dl>
</td>
<td width="60%">
It is known or suspected that the CA's private key or other aspects of the CA validated in the certificate are compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_AFFILIATION_CHANGED"></a><a id="crl_reason_affiliation_changed"></a><dl>
<dt><b>CRL_REASON_AFFILIATION_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
The subject's name or other information in the certificate has been modified but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_SUPERSEDED"></a><a id="crl_reason_superseded"></a><dl>
<dt><b>CRL_REASON_SUPERSEDED</b></dt>
</dl>
</td>
<td width="60%">
The certificate has been superseded, but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_CESSATION_OF_OPERATION"></a><a id="crl_reason_cessation_of_operation"></a><dl>
<dt><b>CRL_REASON_CESSATION_OF_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The certificate is no longer needed for the purpose for which it was issued, but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_CERTIFICATE_HOLD"></a><a id="crl_reason_certificate_hold"></a><dl>
<dt><b>CRL_REASON_CERTIFICATE_HOLD</b></dt>
</dl>
</td>
<td width="60%">
The certificate has been placed on hold.

</td>
</tr>
</table>

### -field fHasFreshnessTime

Depending on <b>cbSize</b>, this structure can contain this member. If this member is <b>TRUE</b>, the revocation freshness time returned by <b>dwFreshnessTime</b> is valid.

### -field dwFreshnessTime

Depending on <b>cbSize</b>, this structure can contain this member. If present, this member gives the time in seconds between the current time and when the CRL was published.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a>