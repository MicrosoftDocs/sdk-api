---
UID: NE:certenroll.X509RequestInheritOptions
title: X509RequestInheritOptions (certenroll.h)
description: Specifies how keys, extension values, and external properties are inherited when a new request is created from an existing certificate.
helpviewer_keywords: ["InheritDefault","InheritExtensionsFlag","InheritKeyMask","InheritNewDefaultKey","InheritNewSimilarKey","InheritNone","InheritPrivateKey","InheritPublicKey","InheritRenewalCertificateFlag","InheritSubjectAltNameFlag","InheritSubjectFlag","InheritTemplateFlag","InheritValidityPeriodFlag","X509RequestInheritOptions","X509RequestInheritOptions enumeration [Security]","certenroll/InheritDefault","certenroll/InheritExtensionsFlag","certenroll/InheritKeyMask","certenroll/InheritNewDefaultKey","certenroll/InheritNewSimilarKey","certenroll/InheritNone","certenroll/InheritPrivateKey","certenroll/InheritPublicKey","certenroll/InheritRenewalCertificateFlag","certenroll/InheritSubjectAltNameFlag","certenroll/InheritSubjectFlag","certenroll/InheritTemplateFlag","certenroll/InheritValidityPeriodFlag","certenroll/X509RequestInheritOptions","security.x509requestinheritoptions_enum"]
old-location: security\x509requestinheritoptions_enum.htm
tech.root: security
ms.assetid: 6aa8d72d-bf6a-476b-812b-9ceafed5e5e7
ms.date: 12/05/2018
ms.keywords: InheritDefault, InheritExtensionsFlag, InheritKeyMask, InheritNewDefaultKey, InheritNewSimilarKey, InheritNone, InheritPrivateKey, InheritPublicKey, InheritRenewalCertificateFlag, InheritSubjectAltNameFlag, InheritSubjectFlag, InheritTemplateFlag, InheritValidityPeriodFlag, X509RequestInheritOptions, X509RequestInheritOptions enumeration [Security], certenroll/InheritDefault, certenroll/InheritExtensionsFlag, certenroll/InheritKeyMask, certenroll/InheritNewDefaultKey, certenroll/InheritNewSimilarKey, certenroll/InheritNone, certenroll/InheritPrivateKey, certenroll/InheritPublicKey, certenroll/InheritRenewalCertificateFlag, certenroll/InheritSubjectAltNameFlag, certenroll/InheritSubjectFlag, certenroll/InheritTemplateFlag, certenroll/InheritValidityPeriodFlag, certenroll/X509RequestInheritOptions, security.x509requestinheritoptions_enum
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: X509RequestInheritOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509RequestInheritOptions
 - certenroll/X509RequestInheritOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509RequestInheritOptions
---

# X509RequestInheritOptions enumeration


## -description

The <b>X509RequestInheritOptions</b> enumeration type specifies how keys, extension values, and external properties are inherited when a new request is created from an existing <a href="/windows/desktop/SecGloss/c-gly">certificate</a>. This enumeration can be used to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a> or an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object from an existing certificate.

You can choose one of the following values to specify how keys are inherited:<ul>
<li><b>InheritNewDefaultKey</b></li>
<li><b>InheritNewSimilarKey</b></li>
<li><b>InheritPrivateKey</b></li>
<li><b>InheritPublicKey</b></li>
</ul>You can also use a bitwise-<b>AND</b> operation to combine the key inheritance choice with  <b>InheritNone</b> or with any combination of the following flags:<ul>
<li><b>InheritRenewalCertificateFlag</b></li>
<li><b>InheritTemplateFlag</b></li>
<li><b>InheritSubjectFlag</b></li>
<li><b>InheritExtensionsFlag</b></li>
<li><b>InheritSubjectAltNameFlag</b></li>
<li><b>InheritValidityPeriodFlag</b></li>
</ul>

## -enum-fields

### -field InheritDefault:0

Inheritance is not specified. For more information, see the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> interface.

### -field InheritNewDefaultKey:0x1

Creates a new key but inherits the default <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) or KSP.

### -field InheritNewSimilarKey:0x2

Creates a new key but inherits the CSP or KSP used to create the existing certificate.

### -field InheritPrivateKey:0x3

Inherits the <a href="/windows/desktop/SecGloss/p-gly">private</a> and <a href="/windows/desktop/SecGloss/p-gly">public keys</a>.

### -field InheritPublicKey:0x4

Inherits only the public key.

### -field InheritKeyMask:0xf

Use to mask the lower-order 4 bits that identify key inheritance.

### -field InheritNone:0x10

Prevents use of the following inheritance values:

<ul>
<li><b>InheritRenewalCertificateFlag</b></li>
<li><b>InheritTemplateFlag</b></li>
<li><b>InheritSubjectFlag</b></li>
<li><b>InheritExtensionsFlag</b></li>
<li><b>InheritSubjectAltNameFlag</b></li>
<li><b>InheritValidityPeriodFlag</b></li>
</ul>

### -field InheritRenewalCertificateFlag:0x20

Inherits the renewal certificate. Specifying this flag sets an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrenewal">ICertPropertyRenewal</a> value.

### -field InheritTemplateFlag:0x40

Inherits the <a href="/windows/desktop/SecGloss/c-gly">certificate template</a>.

### -field InheritSubjectFlag:0x80

Inherits the subject distinguished name.

### -field InheritExtensionsFlag:0x100

Inherits the relevant extensions from the certificate. Extension values associated with the following <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> are not inherited:

<ul>
<li>XCN_OID_CERTSRV_CA_VERSION</li>
<li>XCN_OID_AUTHORITY_INFO_ACCESS</li>
<li>XCN_OID_CRL_DIST_POINTS</li>
<li>XCN_OID_AUTHORITY_KEY_IDENTIFIER2</li>
<li>XCN_OID_CERTSRV_PREVIOUS_CERT_HASH</li>
<li>XCN_OID_ENROLL_CERTTYPE_EXTENSION</li>
<li>XCN_OID_CERTIFICATE_TEMPLATE</li>
</ul>

### -field InheritSubjectAltNameFlag:0x200

Inherits the <b>SubjectAlternativeName</b> extension.

### -field InheritValidityPeriodFlag:0x400

Inherits the validity period.

### -field InheritReserved80000000:0x80000000

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>
