---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_SuppressOids
title: IX509CertificateRequestPkcs10::get_SuppressOids method
author: windows-driver-content
description: Retrieves a collection of the default extension and attribute object identifiers (OIDs) that were not added to the request when the request was encoded.
old-location: security\ix509certificaterequestpkcs10_suppressoids_property.htm
old-project: SecCertEnroll
ms.assetid: 3f7a6d23-00d3-4ab6-817a-a37490f0cb84
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509CertificateRequestPkcs10, IX509CertificateRequestPkcs10 interface [Security], SuppressOids property, IX509CertificateRequestPkcs10.SuppressOids, IX509CertificateRequestPkcs10::get_SuppressOids, SuppressOids property [Security], SuppressOids property [Security], IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::SuppressOids, certenroll/IX509CertificateRequestPkcs10::get_SuppressOids, get_SuppressOids,IX509CertificateRequestPkcs10.get_SuppressOids, security.ix509certificaterequestpkcs10_suppressoids_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestPkcs10.SuppressOids
-	IX509CertificateRequestPkcs10.get_SuppressOids
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_SuppressOids method


## -description


The <b>SuppressOids</b> property retrieves a collection of the default extension and attribute <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) that were not added  to the request when the request was encoded.

This property is read-only.


## -parameters


## -remarks



Attributes and extensions are added to a certificate request when it is encoded or initialized. You can suppress the addition of default extensions and attributes by calling the <a href="https://msdn.microsoft.com/3a7847b6-52b4-4058-8113-cbc3b9101a5b">SuppressDefaults</a> property. For a PKCS #10 request, the following attributes are added by default:

<ul>
<li>XCN_OID_REQUEST_CLIENT_INFO
(<a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a>)</li>
<li>XCN_OID_ENROLLMENT_CSP_PROVIDER (<a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a>)</li>
<li>XCN_OID_OS_VERSION (<a href="https://msdn.microsoft.com/2ae84d47-2bda-4954-9165-902634d09da9">IX509AttributeOSVersion</a>)</li>
<li>XCN_OID_RENEWAL_CERTIFICATE (<a href="https://msdn.microsoft.com/fc432a7a-6ef7-4359-bb53-1ed5df6bc0ab">IX509AttributeRenewalCertificate</a>)</li>
</ul>
The following extensions are added by default:<ul>
<li>XCN_OID_RSA_SMIMECapabilities (<a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a>)</li>
<li>XCN_OID_SUBJECT_KEY_IDENTIFIER
(<a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a>)</li>
<li>XCN_OID_KEY_USAGE (<a href="https://msdn.microsoft.com/4325e6aa-99bb-4c9a-9b19-c5352ebf27b9">IX509ExtensionKeyUsage</a>)</li>
</ul>


You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/10ab62c3-9c6f-4e1b-8a86-131d08282d9c">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b26e69c4-bfe4-4395-aaf6-bc1d045f59cc">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ea746c3-b967-41b4-94ae-7b16b93ca4e4">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

