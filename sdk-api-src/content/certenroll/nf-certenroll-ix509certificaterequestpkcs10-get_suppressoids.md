---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_SuppressOids
title: IX509CertificateRequestPkcs10::get_SuppressOids (certenroll.h)
description: Retrieves a collection of the default extension and attribute object identifiers (OIDs) that were not added to the request when the request was encoded.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","SuppressOids property","IX509CertificateRequestPkcs10.SuppressOids","IX509CertificateRequestPkcs10.get_SuppressOids","IX509CertificateRequestPkcs10::SuppressOids","IX509CertificateRequestPkcs10::get_SuppressOids","SuppressOids property [Security]","SuppressOids property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::SuppressOids","certenroll/IX509CertificateRequestPkcs10::get_SuppressOids","get_SuppressOids","security.ix509certificaterequestpkcs10_suppressoids_property"]
old-location: security\ix509certificaterequestpkcs10_suppressoids_property.htm
tech.root: security
ms.assetid: 3f7a6d23-00d3-4ab6-817a-a37490f0cb84
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],SuppressOids property, IX509CertificateRequestPkcs10.SuppressOids, IX509CertificateRequestPkcs10.get_SuppressOids, IX509CertificateRequestPkcs10::SuppressOids, IX509CertificateRequestPkcs10::get_SuppressOids, SuppressOids property [Security], SuppressOids property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::SuppressOids, certenroll/IX509CertificateRequestPkcs10::get_SuppressOids, get_SuppressOids, security.ix509certificaterequestpkcs10_suppressoids_property
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
 - IX509CertificateRequestPkcs10::get_SuppressOids
 - certenroll/IX509CertificateRequestPkcs10::get_SuppressOids
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
 - IX509CertificateRequestPkcs10.SuppressOids
 - IX509CertificateRequestPkcs10.get_SuppressOids
---

# IX509CertificateRequestPkcs10::get_SuppressOids


## -description

The <b>SuppressOids</b> property retrieves a collection of the default extension and attribute <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) that were not added  to the request when the request was encoded.

This property is read-only.

## -parameters

## -remarks

Attributes and extensions are added to a certificate request when it is encoded or initialized. You can suppress the addition of default extensions and attributes by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_suppressdefaults">SuppressDefaults</a> property. For a PKCS #10 request, the following attributes are added by default:

<ul>
<li>XCN_OID_REQUEST_CLIENT_INFO
(<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>)</li>
<li>XCN_OID_ENROLLMENT_CSP_PROVIDER (<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributecspprovider">IX509AttributeCspProvider</a>)</li>
<li>XCN_OID_OS_VERSION (<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeosversion">IX509AttributeOSVersion</a>)</li>
<li>XCN_OID_RENEWAL_CERTIFICATE (<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributerenewalcertificate">IX509AttributeRenewalCertificate</a>)</li>
</ul>
The following extensions are added by default:<ul>
<li>XCN_OID_RSA_SMIMECapabilities (<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a>)</li>
<li>XCN_OID_SUBJECT_KEY_IDENTIFIER
(<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a>)</li>
<li>XCN_OID_KEY_USAGE (<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a>)</li>
</ul>


You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>