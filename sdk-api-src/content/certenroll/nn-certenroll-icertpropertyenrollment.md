---
UID: NN:certenroll.ICertPropertyEnrollment
title: ICertPropertyEnrollment (certenroll.h)
description: Represents a certificate property that contains certificate and certification authority (CA) information created when the client calls the Enroll method on the IX509Enrollment interface.
helpviewer_keywords: ["ICertPropertyEnrollment","ICertPropertyEnrollment interface [Security]","ICertPropertyEnrollment interface [Security]","described","certenroll/ICertPropertyEnrollment","security.icertpropertyenrollment"]
old-location: security\icertpropertyenrollment.htm
tech.root: security
ms.assetid: 7530998b-b59c-426b-a74a-ead4bca55c3b
ms.date: 12/05/2018
ms.keywords: ICertPropertyEnrollment, ICertPropertyEnrollment interface [Security], ICertPropertyEnrollment interface [Security],described, certenroll/ICertPropertyEnrollment, security.icertpropertyenrollment
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
 - ICertPropertyEnrollment
 - certenroll/ICertPropertyEnrollment
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
 - ICertPropertyEnrollment
---

# ICertPropertyEnrollment interface


## -description

The <b>ICertPropertyEnrollment</b> interface represents a certificate property that contains certificate and certification authority (CA) information created when the client calls the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-enroll">Enroll</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface. The property value consists of the following information:<ul>
<li>A certificate request ID</li>
<li>The common name (CN) of the certificate subject</li>
<li>The certification authority (CA) Domain Name System (DNS) name</li>
<li>The optional display name of the certificate being requested</li>
</ul>


This property is initialized by the enrollment process and associated with the dummy certificate that is temporarily copied to the request store. If the CA marks the request pending after it is submitted, auto-enrollment can later use the request ID to retrieve the certificate response. If the CA denies the certificate request, the dummy certificate in the request store and all properties associated with it are deleted. If the CA issues the certificate and it is installed in the personal store, this property is associated with the new certificate and the dummy certificate is deleted.<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_ENROLLMENT_PROP_ID.</div>
<div> </div>

## -inheritance

The <b>ICertPropertyEnrollment</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyEnrollment</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
