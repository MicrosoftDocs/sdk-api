---
UID: NN:certenroll.IX509ExtensionTemplateName
title: IX509ExtensionTemplateName (certenroll.h)
description: Defines methods and properties that can be used to initialize or retrieve a template name extension.
helpviewer_keywords: ["IX509ExtensionTemplateName","IX509ExtensionTemplateName interface [Security]","IX509ExtensionTemplateName interface [Security]","described","certenroll/IX509ExtensionTemplateName","security.ix509extensiontemplatename"]
old-location: security\ix509extensiontemplatename.htm
tech.root: security
ms.assetid: 9a2d0219-6fe3-4a75-8d28-281c0b863a35
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplateName, IX509ExtensionTemplateName interface [Security], IX509ExtensionTemplateName interface [Security],described, certenroll/IX509ExtensionTemplateName, security.ix509extensiontemplatename
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
 - IX509ExtensionTemplateName
 - certenroll/IX509ExtensionTemplateName
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
 - IX509ExtensionTemplateName
---

# IX509ExtensionTemplateName interface


## -description

The <b>IX509ExtensionTemplateName</b> interface defines methods and properties that can be used to initialize or retrieve a template name extension. This extension can be placed in the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> to tell the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> what template to use when issuing or renewing a certificate. The template is identified by name.<div class="alert"><b>Note</b>  The <b>CertificateTemplateName</b> extension is used to identify version 1 templates. To identify a version 2 template, you can use the <b>CertificateTemplate</b> extension defined by the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a> interface.</div>
<div> </div>


The extension is encoded as a name-value pair where name equals the Unicode string "CertificateTemplate" and the associated value is the name of the template. The following syntax shows an example of the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) output for the template named "User". The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER).

``` syntax

30 42				; SEQUENCE (42 Bytes)
|  06 0a				; OBJECT_ID (a Bytes)
|  |  2b 06 01 04 01 82 37 0d  02 01
|  |     ; 1.3.6.1.4.1.311.13.2.1 Enrollment Name Value Pair
|  31 34				; SET (34 Bytes)
|     30 32			; SEQUENCE (32 Bytes)
|        1e 26			; UNICODE_STRING (26 Bytes)
|        |  00 43 00 65 00 72 00 74  00 69 00 66 00 69 00 63  ; .C.e.r.t.i.f.i.c
|        |  00 61 00 74 00 65 00 54  00 65 00 6d 00 70 00 6c  ; .a.t.e.T.e.m.p.l
|        |  00 61 00 74 00 65                                 ; .a.t.e
|        |     ; "CertificateTemplate"
|        1e 08			; UNICODE_STRING (8 Bytes)
|           00 55 00 73 00 65 00 72                           ; .U.s.e.r
|              ; "User"

```
To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionTemplateName</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionTemplateName</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
