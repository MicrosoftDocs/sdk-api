---
UID: NN:certenroll.IX509CertificateRequest
title: IX509CertificateRequest (certenroll.h)
description: The IX509CertificateRequest interface represents an abstract base certificate request that identifies methods and properties common to and inherited by each of the request objects implemented by the Certificate Enrollment API.
helpviewer_keywords: ["IX509CertificateRequest","IX509CertificateRequest interface [Security]","IX509CertificateRequest interface [Security]","described","certenroll/IX509CertificateRequest","security.ix509certificaterequest"]
old-location: security\ix509certificaterequest.htm
tech.root: security
ms.assetid: 5425c9ab-565d-449d-87e1-e5765868acfb
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequest, IX509CertificateRequest interface [Security], IX509CertificateRequest interface [Security],described, certenroll/IX509CertificateRequest, security.ix509certificaterequest
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
 - IX509CertificateRequest
 - certenroll/IX509CertificateRequest
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
 - IX509CertificateRequest
---

# IX509CertificateRequest interface


## -description

The <b>IX509CertificateRequest</b> interface   represents an abstract base certificate request that identifies methods and properties common to and inherited by each of the request objects implemented by the Certificate Enrollment API. The following list discusses the inheritance structure of these objects:<ul>
<li>
A PKCS #10 certificate request implements the <b>IX509CertificateRequest</b> and <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> interfaces. 

<img alt="Inheritance diagram for a PKCS #10 request object" src="./images/X509Inherit_RequestPkcs10.png"/>

</li>
<li>
 PKCS #7 certificate request implements the <b>IX509CertificateRequest</b> and <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a> interfaces.

<img alt="Inheritance diagram for a PKCS #7 request object" src="./images/X509Inherit_RequestPkcs7.png"/>

Although the PKCS #7 specification defines a secure message syntax rather than a type of certificate request, the implementation of the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a> interface in this SDK requires that it contain a PKCS #10 request. Therefore, this documentation refers to a PKCS #7 object as a certificate request.

</li>
<li>
A CMC (Certificate Management Message over CMS) certificate request implements the <b>IX509CertificateRequest</b>, <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>, and <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a> interfaces.

<img alt="Inheritance diagram for a CMC request object" src="./images/X509Inherit_RequestCMC.png"/>

</li>
<li>
An object that can be used to represent a self-generated certificate (a certificate not issued by a certification authority) implements the <b>IX509CertificateRequest</b>, <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>, and <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a> interfaces.

<img alt="Inheritance diagram for a self-generated certificate" src="./images/X509Inherit_Requestcertificate.png"/>

</li>
</ul>

## -inheritance

The <b>IX509CertificateRequest</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509CertificateRequest</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>
