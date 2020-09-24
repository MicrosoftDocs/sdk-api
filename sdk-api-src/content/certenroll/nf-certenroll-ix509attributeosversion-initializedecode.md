---
UID: NF:certenroll.IX509AttributeOSVersion.InitializeDecode
title: IX509AttributeOSVersion::InitializeDecode (certenroll.h)
description: Initializes the object from a Distinguished Encoding Rules (DER) encoded byte array that contains the operating system version information.
helpviewer_keywords: ["IX509AttributeOSVersion interface [Security]","InitializeDecode method","IX509AttributeOSVersion.InitializeDecode","IX509AttributeOSVersion::InitializeDecode","InitializeDecode","InitializeDecode method [Security]","InitializeDecode method [Security]","IX509AttributeOSVersion interface","certenroll/IX509AttributeOSVersion::InitializeDecode","security.ix509attributeosversioner_initializedecode_method"]
old-location: security\ix509attributeosversioner_initializedecode_method.htm
tech.root: security
ms.assetid: 2f13002f-bdaa-4c82-859a-da932615dd81
ms.date: 12/05/2018
ms.keywords: IX509AttributeOSVersion interface [Security],InitializeDecode method, IX509AttributeOSVersion.InitializeDecode, IX509AttributeOSVersion::InitializeDecode, InitializeDecode, InitializeDecode method [Security], InitializeDecode method [Security],IX509AttributeOSVersion interface, certenroll/IX509AttributeOSVersion::InitializeDecode, security.ix509attributeosversioner_initializedecode_method
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
 - IX509AttributeOSVersion::InitializeDecode
 - certenroll/IX509AttributeOSVersion::InitializeDecode
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
 - IX509AttributeOSVersion.InitializeDecode
---

# IX509AttributeOSVersion::InitializeDecode


## -description

The <b>InitializeDecode</b> method initializes the object from a  <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the operating system version information.  The byte array is represented by a Unicode-encoded string.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string.

### -param strEncodedData [in]

A <b>BSTR</b> variable that contains the DER-encoded attribute.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for this attribute is <b>XCN_OID_OS_VERSION</b> (1.3.6.1.4.1.311.13.2.3). For more information, see <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a>.

You can use this method if you have a DER-encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) object that contains the attribute value. You must supply the DER-encoded object in a Unicode encoded string. For more information, see the <a href="/windows/desktop/api/certenroll/nn-certenroll-ibinaryconverter">IBinaryConverter</a> interface.

You must call either <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeosversion-initializeencode">InitializeEncode</a> or <b>InitializeDecode</b> before you can use an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeosversion">IX509AttributeOSVersion</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded ASN.1 structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeosversion-get_osversion">OSVersion</a> property to retrieve the raw data.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeosversion">IX509AttributeOSVersion</a>