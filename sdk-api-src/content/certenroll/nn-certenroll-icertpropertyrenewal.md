---
UID: NN:certenroll.ICertPropertyRenewal
title: ICertPropertyRenewal (certenroll.h)
description: Represents a certificate property that contains a SHA-1 hash of the new certificate created when an existing certificate is renewed.
helpviewer_keywords: ["ICertPropertyRenewal","ICertPropertyRenewal interface [Security]","ICertPropertyRenewal interface [Security]","described","certenroll/ICertPropertyRenewal","security.icertpropertyrenewal"]
old-location: security\icertpropertyrenewal.htm
tech.root: security
ms.assetid: c87a391a-aec9-4b42-8084-c593ecbb0bc6
ms.date: 12/05/2018
ms.keywords: ICertPropertyRenewal, ICertPropertyRenewal interface [Security], ICertPropertyRenewal interface [Security],described, certenroll/ICertPropertyRenewal, security.icertpropertyrenewal
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
 - ICertPropertyRenewal
 - certenroll/ICertPropertyRenewal
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
 - ICertPropertyRenewal
---

# ICertPropertyRenewal interface


## -description

The <b>ICertPropertyRenewal</b> interface represents a certificate property that contains a SHA-1 hash of the new certificate created when an existing certificate is renewed. This property is associated with the old certificate to identify the new certificate that replaces it.  Typically, the SHA-1 hash is referred to as the thumb print of a certificate.

This property is initialized by the enrollment process after the client requests that a certificate be renewed. If a new certificate is issued, the property is associated with the old certificate in the personal store.<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_RENEWAL_PROP_ID.</div>
<div> </div>

## -inheritance

The <b>ICertPropertyRenewal</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyRenewal</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
