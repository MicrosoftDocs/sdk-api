---
UID: NS:wincrypt._OCSP_BASIC_REVOKED_INFO
title: OCSP_BASIC_REVOKED_INFO (wincrypt.h)
author: windows-sdk-content
description: Contains the reason a certificate was revoked.
old-location: security\ocsp_basic_revoked_info.htm
tech.root: SecCrypto
ms.assetid: 4475cf2a-bf25-427d-8e53-5e5b96dd676a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*POCSP_BASIC_REVOKED_INFO, CRL_REASON_AFFILIATION_CHANGED, CRL_REASON_CA_COMPROMISE, CRL_REASON_CERTIFICATE_HOLD, CRL_REASON_CESSATION_OF_OPERATION, CRL_REASON_KEY_COMPROMISE, CRL_REASON_REMOVE_FROM_CRL, CRL_REASON_SUPERSEDED, CRL_REASON_UNSPECIFIED, OCSP_BASIC_REVOKED_INFO, OCSP_BASIC_REVOKED_INFO structure [Security], POCSP_BASIC_REVOKED_INFO, POCSP_BASIC_REVOKED_INFO structure pointer [Security], security.ocsp_basic_revoked_info, wincrypt/OCSP_BASIC_REVOKED_INFO, wincrypt/POCSP_BASIC_REVOKED_INFO"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - OCSP_BASIC_REVOKED_INFO
product: Windows
targetos: Windows
req.typenames: OCSP_BASIC_REVOKED_INFO, *POCSP_BASIC_REVOKED_INFO
req.redist: 
ms.custom: 19H1
---

# OCSP_BASIC_REVOKED_INFO structure


## -description


The <b>OCSP_BASIC_REVOKED_INFO</b> structure contains the reason a certificate was revoked. The <a href="https://msdn.microsoft.com/c22f25fd-bbee-45de-9ca0-064b159abb7c">OCSP_BASIC_RESPONSE_ENTRY</a> structure uses this structure.


## -struct-fields




### -field RevocationDate

Date that the certificate was revoked. For more information, see the <b>RevocationDate</b> member description for <a href="https://msdn.microsoft.com/30e7952a-a408-404f-9058-8197539387f6">CRL_ENTRY</a>.


### -field dwCrlReasonCode

A value that specifies the reason a certificate was revoked. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_UNSPECIFIED"></a><a id="crl_reason_unspecified"></a><dl>
<dt><b>CRL_REASON_UNSPECIFIED</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No reason was specified for revocation.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_KEY_COMPROMISE"></a><a id="crl_reason_key_compromise"></a><dl>
<dt><b>CRL_REASON_KEY_COMPROMISE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
It is known or suspected that the subject's <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> or other aspects of the subject validated in the certificate are compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_CA_COMPROMISE"></a><a id="crl_reason_ca_compromise"></a><dl>
<dt><b>CRL_REASON_CA_COMPROMISE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
It is known or suspected that the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority's</a> (CA's) private key or other aspects of the CA validated in the certificate are compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_AFFILIATION_CHANGED"></a><a id="crl_reason_affiliation_changed"></a><dl>
<dt><b>CRL_REASON_AFFILIATION_CHANGED</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The subject's name or other information in the certificate has been modified but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_SUPERSEDED"></a><a id="crl_reason_superseded"></a><dl>
<dt><b>CRL_REASON_SUPERSEDED</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The certificate has been superseded, but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_CESSATION_OF_OPERATION"></a><a id="crl_reason_cessation_of_operation"></a><dl>
<dt><b>CRL_REASON_CESSATION_OF_OPERATION</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The certificate is no longer needed for the purpose for which it was issued, but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_CERTIFICATE_HOLD"></a><a id="crl_reason_certificate_hold"></a><dl>
<dt><b>CRL_REASON_CERTIFICATE_HOLD</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The certificate has been placed on hold.

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_REASON_REMOVE_FROM_CRL"></a><a id="crl_reason_remove_from_crl"></a><dl>
<dt><b>CRL_REASON_REMOVE_FROM_CRL</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The certificate has been removed from the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL).

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/30e7952a-a408-404f-9058-8197539387f6">CRL_ENTRY</a>



<a href="https://msdn.microsoft.com/c22f25fd-bbee-45de-9ca0-064b159abb7c">OCSP_BASIC_RESPONSE_ENTRY</a>
 

 

