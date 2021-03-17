---
UID: NF:certadm.ICertAdmin.GetRevocationReason
title: ICertAdmin::GetRevocationReason (certadm.h)
description: Returns the reason a certificate was revoked. This method was first defined in the ICertAdmin interface.
helpviewer_keywords: ["CCertAdmin object [Security]","GetRevocationReason method","GetRevocationReason","GetRevocationReason method [Security]","GetRevocationReason method [Security]","CCertAdmin object","GetRevocationReason method [Security]","ICertAdmin interface","GetRevocationReason method [Security]","ICertAdmin2 interface","ICertAdmin interface [Security]","GetRevocationReason method","ICertAdmin.GetRevocationReason","ICertAdmin2 interface [Security]","GetRevocationReason method","ICertAdmin2::GetRevocationReason","ICertAdmin::GetRevocationReason","certadm/ICertAdmin2::GetRevocationReason","certadm/ICertAdmin::GetRevocationReason","security.icertadmin2_getrevocationreason"]
old-location: security\icertadmin2_getrevocationreason.htm
tech.root: security
ms.assetid: 244b121a-76ba-44fd-b15d-f076b722b030
ms.date: 12/05/2018
ms.keywords: CCertAdmin object [Security],GetRevocationReason method, GetRevocationReason, GetRevocationReason method [Security], GetRevocationReason method [Security],CCertAdmin object, GetRevocationReason method [Security],ICertAdmin interface, GetRevocationReason method [Security],ICertAdmin2 interface, ICertAdmin interface [Security],GetRevocationReason method, ICertAdmin.GetRevocationReason, ICertAdmin2 interface [Security],GetRevocationReason method, ICertAdmin2::GetRevocationReason, ICertAdmin::GetRevocationReason, certadm/ICertAdmin2::GetRevocationReason, certadm/ICertAdmin::GetRevocationReason, security.icertadmin2_getrevocationreason
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin::GetRevocationReason
 - certadm/ICertAdmin::GetRevocationReason
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.GetRevocationReason
 - ICertAdmin.GetRevocationReason
 - CCertAdmin.GetRevocationReason
---

# ICertAdmin::GetRevocationReason


## -description

The <b>GetRevocationReason</b> method  returns  the reason a certificate was revoked. This method was first defined in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

Before you call this method, you must call the 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin-isvalidcertificate">IsValidCertificate</a> method. For more information, see Remarks.

## -parameters

### -param pReason [out]

A pointer to a variable that will receive the revocation reason.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and  the <i>pReason</i> parameter is set to one of the values listed in the following table.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a value that specifies the reason the certificate was revoked. The value can be one of the following revocation reason codes (defined in Wincrypt.h).

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
No reason was specified for revocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_KEY_COMPROMISE</b></dt>
</dl>
</td>
<td width="60%">
It is known or suspected that the subject's private key or other aspects of the subject validated in the certificate are compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_CA_COMPROMISE</b></dt>
</dl>
</td>
<td width="60%">
It is known or suspected that the CA's private key or other aspects of the CA validated in the certificate are compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_AFFILIATION_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
The subject's name or other information in the certificate has been modified but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_SUPERSEDED</b></dt>
</dl>
</td>
<td width="60%">
The certificate has been superseded, but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_CESSATION_OF_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The certificate is no longer needed for the purpose for which it was issued, but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_CERTIFICATE_HOLD</b></dt>
</dl>
</td>
<td width="60%">
The certificate has been placed on hold.

</td>
</tr>
</table>

## -remarks

Before you call <b>GetRevocationReason</b>, call the 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin-isvalidcertificate">IsValidCertificate</a> method to retrieve the disposition of the certificate. To call <b>GetRevocationReason</b>, you must receive a certificate disposition CA_DISP_REVOKED from this earlier call, indicating that the certificate has been revoked. The call to <b>IsValidCertificate</b> establishes the identity of the certificate whose revocation reason you want to retrieve.

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples


```cpp
// The value for nDisp was set by 
// a call to ICertAdmin2::IsValidCertificate.
if (CA_DISP_REVOKED == nDisp)
{
    // Variable to contain revocation reason.
    long       nReason;

    // Retrieve the revocation reason.
    hr = pCertAdmin->GetRevocationReason(&nReason);
    if (FAILED(hr))
    {
        printf("Failed GetRevocationReason [%x]\n", hr);
        goto error;
    }
    else
        printf("Revocation reason = %d\n", nReason );
}
```

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">CCertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>



<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin-isvalidcertificate">IsValidCertificate</a>