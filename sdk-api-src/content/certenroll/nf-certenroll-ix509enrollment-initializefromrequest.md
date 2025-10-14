---
UID: NF:certenroll.IX509Enrollment.InitializeFromRequest
title: IX509Enrollment::InitializeFromRequest (certenroll.h)
description: Initializes the enrollment object from an existing IX509CertificateRequest object.
helpviewer_keywords: ["IX509Enrollment interface [Security]","InitializeFromRequest method","IX509Enrollment.InitializeFromRequest","IX509Enrollment::InitializeFromRequest","InitializeFromRequest","InitializeFromRequest method [Security]","InitializeFromRequest method [Security]","IX509Enrollment interface","certenroll/IX509Enrollment::InitializeFromRequest","security.ix509enrollment_initializefromrequest_method"]
old-location: security\ix509enrollment_initializefromrequest_method.htm
tech.root: security
ms.assetid: 04cb00af-f786-4548-bee3-2cc5083278c3
ms.date: 12/05/2018
ms.keywords: IX509Enrollment interface [Security],InitializeFromRequest method, IX509Enrollment.InitializeFromRequest, IX509Enrollment::InitializeFromRequest, InitializeFromRequest, InitializeFromRequest method [Security], InitializeFromRequest method [Security],IX509Enrollment interface, certenroll/IX509Enrollment::InitializeFromRequest, security.ix509enrollment_initializefromrequest_method
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
 - IX509Enrollment::InitializeFromRequest
 - certenroll/IX509Enrollment::InitializeFromRequest
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
 - IX509Enrollment.InitializeFromRequest
---

# IX509Enrollment::InitializeFromRequest


## -description

The <b>InitializeFromRequest</b> method initializes the enrollment object from an existing <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> object. This method is web enabled.

## -parameters

### -param pRequest [in]

Pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> interface.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The enrollment object has already been initialized.

</td>
</tr>
</table>

## -remarks

The <b>InitializeFromRequest</b>  method:

<ul>
<li>Verifies that the request is a PKCS #10, PKCS #7, or CMC request object.</li>
<li>Retrieves the template, if any, associated with the request.</li>
<li>Validates the template.</li>
<li>Sets the request object on the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_request">Request</a> property.</li>
<li>Retrieves the signature count, issuance policies, and application policies from the template.</li>
<li>Retrieves the renewal certificate if one exists.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>