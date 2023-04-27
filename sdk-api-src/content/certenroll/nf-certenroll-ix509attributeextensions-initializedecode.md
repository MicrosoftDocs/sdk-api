---
UID: NF:certenroll.IX509AttributeExtensions.InitializeDecode
title: IX509AttributeExtensions::InitializeDecode (certenroll.h)
description: Initializes the object from a Distinguished Encoding Rules (DER) encoded byte array that contains the attribute value. (IX509AttributeExtensions.InitializeDecode)
helpviewer_keywords: ["IX509AttributeExtensions interface [Security]","InitializeDecode method","IX509AttributeExtensions.InitializeDecode","IX509AttributeExtensions::InitializeDecode","InitializeDecode","InitializeDecode method [Security]","InitializeDecode method [Security]","IX509AttributeExtensions interface","certenroll/IX509AttributeExtensions::InitializeDecode","security.ix509attributeextensions_initializedecode_method"]
old-location: security\ix509attributeextensions_initializedecode_method.htm
tech.root: security
ms.assetid: 194f8556-9e26-4fae-ac2b-6c3f07cb22c8
ms.date: 12/05/2018
ms.keywords: IX509AttributeExtensions interface [Security],InitializeDecode method, IX509AttributeExtensions.InitializeDecode, IX509AttributeExtensions::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509AttributeExtensions interface, certenroll/IX509AttributeExtensions::InitializeDecode, security.ix509attributeextensions_initializedecode_method
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
 - IX509AttributeExtensions::InitializeDecode
 - certenroll/IX509AttributeExtensions::InitializeDecode
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
 - IX509AttributeExtensions.InitializeDecode
---

# IX509AttributeExtensions::InitializeDecode


## -description

The <b>InitializeDecode</b> method initializes the object from a  <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the attribute value. The byte array is represented by a Unicode-encoded string.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to  the input string.

### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the encoded extensions.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for this attribute is <b>XCN_OID_RSA_certExtensions</b> (1.2.840.113549.1.9.14). For more information, see <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a>.

You can use this method if you have a DER-encoded ASN.1 object that contains an attribute value. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="/windows/desktop/api/certenroll/nn-certenroll-ibinaryconverter">IBinaryConverter</a> interface.

You must call either <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-initializeencode">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure that contains the certificate extensions. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-get_x509extensions">X509Extensions</a> property to retrieve the extensions.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ibinaryconverter">IBinaryConverter</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
