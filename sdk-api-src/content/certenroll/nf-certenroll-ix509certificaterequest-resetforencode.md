---
UID: NF:certenroll.IX509CertificateRequest.ResetForEncode
title: IX509CertificateRequest::ResetForEncode (certenroll.h)
description: Restores the state of the request object to that which existed before the Encode method was called.
helpviewer_keywords: ["IX509CertificateRequest interface [Security]","ResetForEncode method","IX509CertificateRequest.ResetForEncode","IX509CertificateRequest::ResetForEncode","ResetForEncode","ResetForEncode method [Security]","ResetForEncode method [Security]","IX509CertificateRequest interface","certenroll/IX509CertificateRequest::ResetForEncode","security.ix509certificaterequest_resetforencode_method"]
old-location: security\ix509certificaterequest_resetforencode_method.htm
tech.root: security
ms.assetid: 7f0bd391-c456-467a-8bc1-6f0a8bd21e24
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequest interface [Security],ResetForEncode method, IX509CertificateRequest.ResetForEncode, IX509CertificateRequest::ResetForEncode, ResetForEncode, ResetForEncode method [Security], ResetForEncode method [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::ResetForEncode, security.ix509certificaterequest_resetforencode_method
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509CertificateRequest::ResetForEncode
 - certenroll/IX509CertificateRequest::ResetForEncode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequest.ResetForEncode
---

# IX509CertificateRequest::ResetForEncode


## -description

The <b>ResetForEncode</b> method restores the state of the request object to that which existed before the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method was called.



## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Certificate extensions and attributes have not been defined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object is not encoded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>

## -remarks

You can use this method to reconfigure (re-encode and re-sign) a certificate request in response to rejection of the request by a certification authority.  The signature and the raw data are cleared. The extensions and attributes are reset to the values they had before the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method was called, but critical extension flags are not. For a CMC request object, each nested request is also reset.

This method is typically used for a CMC key archival request when the private key is encrypted and included in the request.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
