---
UID: NF:certenroll.IX509AttributeExtensions.InitializeEncode
title: IX509AttributeExtensions::InitializeEncode (certenroll.h)
description: Initializes the object from an IX509Extensions collection.
helpviewer_keywords: ["IX509AttributeExtensions interface [Security]","InitializeEncode method","IX509AttributeExtensions.InitializeEncode","IX509AttributeExtensions::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509AttributeExtensions interface","certenroll/IX509AttributeExtensions::InitializeEncode","security.ix509attributeextensions_initializeencode_method"]
old-location: security\ix509attributeextensions_initializeencode_method.htm
tech.root: security
ms.assetid: f5b6f0b9-ca49-42f2-842c-34c2445c3824
ms.date: 12/05/2018
ms.keywords: IX509AttributeExtensions interface [Security],InitializeEncode method, IX509AttributeExtensions.InitializeEncode, IX509AttributeExtensions::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeExtensions interface, certenroll/IX509AttributeExtensions::InitializeEncode, security.ix509attributeextensions_initializeencode_method
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
 - IX509AttributeExtensions::InitializeEncode
 - certenroll/IX509AttributeExtensions::InitializeEncode
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
 - IX509AttributeExtensions.InitializeEncode
---

# IX509AttributeExtensions::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the object from an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection.

## -parameters

### -param pExtensions [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> interface that contains the collection.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> for this attribute is <b>XCN_OID_RSA_certExtensions</b> (1.2.840.113549.1.9.14). For more information, see <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-initializedecode">InitializeDecode</a> before you can use an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure that contains the certificate extensions. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-get_x509extensions">X509Extensions</a> property to retrieve the extensions.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>