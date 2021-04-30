---
UID: NF:certenroll.IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob
title: IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob (certenroll.h)
description: Initializes the attribute from an encrypted private key.
helpviewer_keywords: ["IX509AttributeArchiveKeyHash interface [Security]","InitializeEncodeFromEncryptedKeyBlob method","IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob","IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob","InitializeEncodeFromEncryptedKeyBlob","InitializeEncodeFromEncryptedKeyBlob method [Security]","InitializeEncodeFromEncryptedKeyBlob method [Security]","IX509AttributeArchiveKeyHash interface","certenroll/IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob","security.ix509attributearchivekeyhash_initializeencodefromencryptedkeyblob_method"]
old-location: security\ix509attributearchivekeyhash_initializeencodefromencryptedkeyblob_method.htm
tech.root: security
ms.assetid: 2101f15f-b71b-4dea-8ec8-2d3c1926ae15
ms.date: 12/05/2018
ms.keywords: IX509AttributeArchiveKeyHash interface [Security],InitializeEncodeFromEncryptedKeyBlob method, IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob, IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob, InitializeEncodeFromEncryptedKeyBlob, InitializeEncodeFromEncryptedKeyBlob method [Security], InitializeEncodeFromEncryptedKeyBlob method [Security],IX509AttributeArchiveKeyHash interface, certenroll/IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob, security.ix509attributearchivekeyhash_initializeencodefromencryptedkeyblob_method
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
 - IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob
 - certenroll/IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob
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
 - IX509AttributeArchiveKeyHash.InitializeEncodeFromEncryptedKeyBlob
---

# IX509AttributeArchiveKeyHash::InitializeEncodeFromEncryptedKeyBlob


## -description

The <b>InitializeEncodeFromEncryptedKeyBlob</b> method initializes the attribute from an encrypted <a href="/windows/desktop/SecGloss/p-gly">private key</a>. The method computes a SHA-1 <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the private key.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the key.

### -param strEncryptedKeyBlob [in]

A <b>BSTR</b> variable that contains the encrypted key.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for this attribute is <b>XCN_OID_ENCRYPTED_KEY_HASH</b> (1.3.6.1.4.1.311.21.21). For more information, see <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncodeFromEncryptedKeyBlob</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekeyhash-initializedecode">InitializeDecode</a> before you can use an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekeyhash">IX509AttributeArchiveKeyHash</a> object. The two methods complement each other. The <b>InitializeEncodeFromEncryptedKeyBlob</b> method enables you to construct an encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekeyhash-get_encryptedkeyhashblob">EncryptedKeyHashBlob</a> property to retrieve the raw data.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekeyhash">IX509AttributeArchiveKeyHash</a>