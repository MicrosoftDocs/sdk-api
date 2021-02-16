---
UID: NF:certenroll.IX509AttributeArchiveKey.InitializeEncode
title: IX509AttributeArchiveKey::InitializeEncode (certenroll.h)
description: Initializes the attribute from an IX509PrivateKey object, the certification authority encryption certificate, and the symmetric encryption algorithm object identifier (OID).
helpviewer_keywords: ["IX509AttributeArchiveKey interface [Security]","InitializeEncode method","IX509AttributeArchiveKey.InitializeEncode","IX509AttributeArchiveKey::InitializeEncode","InitializeEncode","InitializeEncode method [Security]","InitializeEncode method [Security]","IX509AttributeArchiveKey interface","certenroll/IX509AttributeArchiveKey::InitializeEncode","security.ix509attributearchivekey_initializeencode_method"]
old-location: security\ix509attributearchivekey_initializeencode_method.htm
tech.root: security
ms.assetid: 44865c22-0eca-4781-962c-a10698a435f4
ms.date: 12/05/2018
ms.keywords: IX509AttributeArchiveKey interface [Security],InitializeEncode method, IX509AttributeArchiveKey.InitializeEncode, IX509AttributeArchiveKey::InitializeEncode, InitializeEncode, InitializeEncode method [Security], InitializeEncode method [Security],IX509AttributeArchiveKey interface, certenroll/IX509AttributeArchiveKey::InitializeEncode, security.ix509attributearchivekey_initializeencode_method
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
 - IX509AttributeArchiveKey::InitializeEncode
 - certenroll/IX509AttributeArchiveKey::InitializeEncode
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
 - IX509AttributeArchiveKey.InitializeEncode
---

# IX509AttributeArchiveKey::InitializeEncode


## -description

The <b>InitializeEncode</b> method initializes the attribute from an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object, the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> encryption certificate, and the symmetric encryption algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

## -parameters

### -param pKey [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> interface that represents the key.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode encoding applied to the input string that contains the encrypted key.

### -param strCAXCert [in]

A <b>BSTR</b> variable that contains the certification authority encryption certificate that contains the <a href="/windows/desktop/SecGloss/p-gly">public key</a> used to encrypt the private key.

Beginning with Windows 7 and Windows Server 2008 R2, you can specify a certificate thumb print or serial number rather than an encoded certificate. Doing so causes the function to search the appropriate local stores for the matching certificate. Keep in mind the following points:

<ul>
<li>The <b>BSTR</b> must be an even number of hexadecimal digits.</li>
<li>Whitespace between hexadecimal pairs is ignored.</li>
<li>The <i>Encoding</i> parameter must be set to <b>XCN_CRYPT_STRING_HEXRAW</b>.</li>
<li>Only the personal and request stores are searched for the private key.</li>
</ul>

### -param pAlgorithm [in, optional]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that represents the OID of the symmetric encryption algorithm used to encrypt the <a href="/windows/desktop/SecGloss/p-gly">private key</a>. This parameter is optional. If you do not supply an OID, XCN_OID_RSA_DES_EDE3_CBC (Triple DES) is used.

### -param EncryptionStrength [in]

A <b>LONG</b> variable that contains the encryption strength of the algorithm identified by the <i>pAlgorithm</i> parameter. This parameter is not currently used because the Certificate Enrollment SDK does not support any algorithms for which the OID does not already imply the strength (key length). For example, AES has multiple strengths but strength each is already indicated by the OID.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The object identifier for this attribute is <b>XCN_OID_ARCHIVED_KEY_ATTR</b> (1.3.6.1.4.1.311.21.13). For more information, see <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_objectid">CERTENROLL_OBJECTID</a>.

You must call either <b>InitializeEncode</b> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-initializedecode">InitializeDecode</a> before you can use an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a> object. The two methods complement each other. The <b>InitializeEncode</b> method enables you to construct an encoded <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure from raw data, and the <b>InitializeDecode</b> method enables you to initialize raw data from an encoded ASN.1 structure. You can call the following properties to retrieve the raw data:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptionalgorithm">EncryptionAlgorithm</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptedkeyblob">EncryptedKeyBlob</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributearchivekey-get_encryptionstrength">EncryptionStrength</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>