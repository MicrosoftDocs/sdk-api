---
UID: NN:certenroll.IX509ExtensionTemplate
title: IX509ExtensionTemplate (certenroll.h)
description: Defines methods and properties that can be used to initialize or retrieve a CertificateTemplate extension.
helpviewer_keywords: ["IX509ExtensionTemplate","IX509ExtensionTemplate interface [Security]","IX509ExtensionTemplate interface [Security]","described","certenroll/IX509ExtensionTemplate","security.ix509extensiontemplate"]
old-location: security\ix509extensiontemplate.htm
tech.root: security
ms.assetid: 2ac24ee9-f31f-4501-a4f0-321580ec2fa9
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplate, IX509ExtensionTemplate interface [Security], IX509ExtensionTemplate interface [Security],described, certenroll/IX509ExtensionTemplate, security.ix509extensiontemplate
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
 - IX509ExtensionTemplate
 - certenroll/IX509ExtensionTemplate
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
 - IX509ExtensionTemplate
---

# IX509ExtensionTemplate interface


## -description

The <b>IX509ExtensionTemplate</b> interface defines methods and properties that can be used to initialize or retrieve a <b>CertificateTemplate</b> extension. This extension can be placed in the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> to tell the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> what template to use when issuing or renewing a certificate. <div class="alert"><b>Note</b>  The <b>CertificateTemplate</b> extension is used to identify version 2 templates. To identify a version 1 template, you can use the <b>CertificateTemplateName</b> extension defined by the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a> interface.</div>
<div> </div>The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the certificate request.

``` syntax

----------------------------------------------------------------------
-- CertificateTemplate
-- XCN_OID_CERTIFICATE_TEMPLATE (1.3.6.1.4.1.311.21.7)
----------------------------------------------------------------------

CertificateTemplate ::= SEQUENCE 
{
   templateID              EncodedObjectID,
   templateMajorVersion    TemplateVersion,
   templateMinorVersion    TemplateVersion OPTIONAL
}

TemplateVersion ::= INTEGER (0..4294967295)

```
To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionTemplate</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionTemplate</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
