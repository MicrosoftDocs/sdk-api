---
UID: NF:certenroll.IX509CertificateRequest.GetInnerRequest
title: IX509CertificateRequest::GetInnerRequest (certenroll.h)
description: Retrieves a nested request object.
helpviewer_keywords: ["GetInnerRequest","GetInnerRequest method [Security]","GetInnerRequest method [Security]","IX509CertificateRequest interface","IX509CertificateRequest interface [Security]","GetInnerRequest method","IX509CertificateRequest.GetInnerRequest","IX509CertificateRequest::GetInnerRequest","certenroll/IX509CertificateRequest::GetInnerRequest","security.ix509certificaterequest_getinnerrequest_method"]
old-location: security\ix509certificaterequest_getinnerrequest_method.htm
tech.root: security
ms.assetid: 5ade7824-d95a-492d-aadf-487422386500
ms.date: 12/05/2018
ms.keywords: GetInnerRequest, GetInnerRequest method [Security], GetInnerRequest method [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],GetInnerRequest method, IX509CertificateRequest.GetInnerRequest, IX509CertificateRequest::GetInnerRequest, certenroll/IX509CertificateRequest::GetInnerRequest, security.ix509certificaterequest_getinnerrequest_method
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
 - IX509CertificateRequest::GetInnerRequest
 - certenroll/IX509CertificateRequest::GetInnerRequest
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
 - IX509CertificateRequest.GetInnerRequest
---

# IX509CertificateRequest::GetInnerRequest


## -description

The <b>GetInnerRequest</b> method retrieves a nested request object.

## -parameters

### -param Level [in]

 A value of an <a href="/windows/desktop/api/certenroll/ne-certenroll-innerrequestlevel">InnerRequestLevel</a> enumeration that specifies the envelopment level of the data to retrieve. You can use the <i>LevelNext</i> value to iterate through the nested levels or the <i>LevelInnermost</i> value to retrieve the most deeply nested request object. You cannot specify <i>LevelNext</i> for a PKCS #10 request.

### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> interface that contains the nested request. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_type">Type</a> property to determine whether the inner request object is a PKCS #10 or a CMC request. Then call <b>QueryInterface</b> to retrieve the appropriate pointer.

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
You specified a value of <i>LevelNext</i> PKCS #10 request.

</td>
</tr>
</table>

## -remarks

A top-level request object can be a PKCS #10, PKCS #7, or CMC request. The following rules apply to inner request objects:<ul>
<li>A PKCS #10 request cannot contain an inner request object.</li>
<li>A PKCS #7 request can contain only a PKCS #10 inner request object.</li>
<li>A CMC request can contain a CMC or a PKCS #10 inner request object. For a CMC request that contains an inner CMC request, there is no theoretical limit to the number of nested levels that can exist before the final inner PKCS #10 request is reached. That is, a top-level CMC request can contain an inner CMC request that also contains an inner CMC request and so on.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>