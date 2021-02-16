---
UID: NF:certenroll.IX509AttributeCspProvider.InitializeEncode
title: IX509AttributeCspProvider::InitializeEncode (certenroll.h)
description: Initializes the attribute from information about the provider.
helpviewer_keywords: ["IX509AttributeCspProvider interface [Security]","InitializeEncode method","IX509AttributeCspProvider.InitializeEncode","IX509AttributeCspProvider::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509AttributeCspProvider interface","certenroll/IX509AttributeCspProvider::InitializeEncode","security.ix509attributecspprovider_initializeencode_method"]
old-location: security\ix509attributecspprovider_initializeencode_method.htm
tech.root: security
ms.assetid: b0b45ea2-b682-4065-8624-08c34581b5ea
ms.date: 12/05/2018
ms.keywords: IX509AttributeCspProvider interface [Security],InitializeEncode method, IX509AttributeCspProvider.InitializeEncode, IX509AttributeCspProvider::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::InitializeEncode, security.ix509attributecspprovider_initializeencode_method
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
 - IX509AttributeCspProvider::InitializeEncode
 - certenroll/IX509AttributeCspProvider::InitializeEncode
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
 - IX509AttributeCspProvider.InitializeEncode
---

# IX509AttributeCspProvider::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the attribute from information about the provider.

## -parameters

### -param KeySpec [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509keyspec">X509KeySpec</a> enumeration value that identifies whether the key pair is used for encryption or for signing.

### -param strProviderName [in]

A <b>BSTR</b> variable that contains the provider name.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the signature contained in the <i>strSignature</i> parameter.

### -param strSignature [in]

A <b>BSTR</b> variable that contains the provider signature.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for this attribute is <b>XCN_OID_ENROLLMENT_CSP_PROVIDER</b> (1.3.6.1.4.1.311.13.2.2). For more information, see <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializedecode">InitializeDecode</a> before you can use an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributecspprovider">IX509AttributeCspProvider</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_keyspec">KeySpec</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_providername">ProviderName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_signature">Signature</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributecspprovider">IX509AttributeCspProvider</a>