---
UID: NN:certenroll.ICryptAttribute
title: ICryptAttribute (certenroll.h)
description: The ICryptAttribute interface represents a cryptographic attribute in a certificate request. A collection of these attributes is contained in the CertificateRequestInfo structure of a PKCS
helpviewer_keywords: ["ICryptAttribute","ICryptAttribute interface [Security]","ICryptAttribute interface [Security]","described","certenroll/ICryptAttribute","security.icryptattribute"]
old-location: security\icryptattribute.htm
tech.root: security
ms.assetid: 2aefde1b-0f77-4a88-8851-5bacd363900b
ms.date: 12/05/2018
ms.keywords: ICryptAttribute, ICryptAttribute interface [Security], ICryptAttribute interface [Security],described, certenroll/ICryptAttribute, security.icryptattribute
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
 - ICryptAttribute
 - certenroll/ICryptAttribute
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
 - ICryptAttribute
---

# ICryptAttribute interface


## -description

The <b>ICryptAttribute</b> interface represents a cryptographic attribute in a certificate request. A collection of these attributes is contained in the  <b>CertificateRequestInfo</b> structure of a  PKCS #10 request as shown by the following example syntax.

``` syntax

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY, 
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

AttributeSetValue ::= SET OF ANY

```
A single <b>ICryptAttribute</b> object corresponds to the attributes collection in the request. The <b>ICryptAttribute</b> object in turn contains a collection of <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a> objects. Each attribute in this collection contains an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> and one or more values. Each value is an encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure. Zero or more of the following objects can be included in the collection:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekeyhash">IX509AttributeArchiveKeyHash</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributecspprovider">IX509AttributeCspProvider</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeosversion">IX509AttributeOSVersion</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributerenewalcertificate">IX509AttributeRenewalCertificate</a>
</li>
</ul>

## -inheritance

The <b>ICryptAttribute</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICryptAttribute</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
