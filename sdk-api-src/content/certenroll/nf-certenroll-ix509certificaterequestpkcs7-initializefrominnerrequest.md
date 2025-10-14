---
UID: NF:certenroll.IX509CertificateRequestPkcs7.InitializeFromInnerRequest
title: IX509CertificateRequestPkcs7::InitializeFromInnerRequest (certenroll.h)
description: Initializes the certificate request from the inner PKCS
helpviewer_keywords: ["IX509CertificateRequestPkcs7 interface [Security]","InitializeFromInnerRequest method","IX509CertificateRequestPkcs7.InitializeFromInnerRequest","IX509CertificateRequestPkcs7::InitializeFromInnerRequest","InitializeFromInnerRequest","InitializeFromInnerRequest method [Security]","InitializeFromInnerRequest method [Security]","IX509CertificateRequestPkcs7 interface","certenroll/IX509CertificateRequestPkcs7::InitializeFromInnerRequest","security.ix509certificaterequestpkcs7_initializefrominnerrequest_method"]
old-location: security\ix509certificaterequestpkcs7_initializefrominnerrequest_method.htm
tech.root: security
ms.assetid: b63bfaaa-a8af-4c72-a191-447230adae72
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs7 interface [Security],InitializeFromInnerRequest method, IX509CertificateRequestPkcs7.InitializeFromInnerRequest, IX509CertificateRequestPkcs7::InitializeFromInnerRequest, InitializeFromInnerRequest, InitializeFromInnerRequest method [Security], InitializeFromInnerRequest method [Security],IX509CertificateRequestPkcs7 interface, certenroll/IX509CertificateRequestPkcs7::InitializeFromInnerRequest, security.ix509certificaterequestpkcs7_initializefrominnerrequest_method
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
 - IX509CertificateRequestPkcs7::InitializeFromInnerRequest
 - certenroll/IX509CertificateRequestPkcs7::InitializeFromInnerRequest
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
 - IX509CertificateRequestPkcs7.InitializeFromInnerRequest
---

# IX509CertificateRequestPkcs7::InitializeFromInnerRequest


## -description

The <b>InitializeFromInnerRequest</b> method initializes the certificate request  from the inner PKCS #10 object. This method is web enabled.

## -parameters

### -param pInnerRequest [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> interface that represents the request.

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
<dt><b>CRYPT_E_INVALID_MSG_TYPE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object specified on input is not a PKCS #10 request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object has already been initialized.

</td>
</tr>
</table>

## -remarks

This method sets the inner request object to the PKCS #10 request specified on input.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>