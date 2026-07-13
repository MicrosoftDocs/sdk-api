---
UID: NN:certenroll.IX509CertificateRequestCertificate
title: IX509CertificateRequestCertificate (certenroll.h)
description: The IX509CertificateRequestCertificate interface represents a request object for a self-generated certificate, enabling you to create a certificate directly without going through a registration or certification authority.
helpviewer_keywords: ["IX509CertificateRequestCertificate","IX509CertificateRequestCertificate interface [Security]","IX509CertificateRequestCertificate interface [Security]","described","certenroll/IX509CertificateRequestCertificate","security.ix509certificaterequestcertificate"]
old-location: security\ix509certificaterequestcertificate.htm
tech.root: security
ms.assetid: 7197a225-b2dc-47bb-8843-d3fb4bf95811
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCertificate, IX509CertificateRequestCertificate interface [Security], IX509CertificateRequestCertificate interface [Security],described, certenroll/IX509CertificateRequestCertificate, security.ix509certificaterequestcertificate
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
 - IX509CertificateRequestCertificate
 - certenroll/IX509CertificateRequestCertificate
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
 - IX509CertificateRequestCertificate
---

# IX509CertificateRequestCertificate interface


## -description

The <b>IX509CertificateRequestCertificate</b> interface represents a request object for a self-generated certificate, enabling you to create a certificate directly without going through a registration or certification authority. The following illustration shows the inheritance structure for this object.

<img alt="Inheritance diagram for a self-generated certificate" src="./images/X509Inherit_Requestcertificate.png"/>

## -inheritance

The <b>IX509CertificateRequestCertificate</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>. <b>IX509CertificateRequestCertificate</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
