---
UID: NF:certenroll.IX509PublicKey.get_EncodedParameters
title: IX509PublicKey::get_EncodedParameters (certenroll.h)
description: Retrieves a byte array that contains the parameters associated with the public key algorithm.
helpviewer_keywords: ["EncodedParameters property [Security]","EncodedParameters property [Security]","IX509PublicKey interface","IX509PublicKey interface [Security]","EncodedParameters property","IX509PublicKey.EncodedParameters","IX509PublicKey.get_EncodedParameters","IX509PublicKey::EncodedParameters","IX509PublicKey::get_EncodedParameters","certenroll/IX509PublicKey::EncodedParameters","certenroll/IX509PublicKey::get_EncodedParameters","get_EncodedParameters","security.ix509publickey_encodedparameters_property"]
old-location: security\ix509publickey_encodedparameters_property.htm
tech.root: security
ms.assetid: f7c7bf0a-0b66-4676-9448-f74937823f90
ms.date: 12/05/2018
ms.keywords: EncodedParameters property [Security], EncodedParameters property [Security],IX509PublicKey interface, IX509PublicKey interface [Security],EncodedParameters property, IX509PublicKey.EncodedParameters, IX509PublicKey.get_EncodedParameters, IX509PublicKey::EncodedParameters, IX509PublicKey::get_EncodedParameters, certenroll/IX509PublicKey::EncodedParameters, certenroll/IX509PublicKey::get_EncodedParameters, get_EncodedParameters, security.ix509publickey_encodedparameters_property
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
 - IX509PublicKey::get_EncodedParameters
 - certenroll/IX509PublicKey::get_EncodedParameters
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
 - IX509PublicKey.EncodedParameters
 - IX509PublicKey.get_EncodedParameters
---

# IX509PublicKey::get_EncodedParameters


## -description

The <b>EncodedParameters</b> property retrieves a byte array that contains the parameters associated with the <a href="/windows/desktop/SecGloss/p-gly">public key</a> algorithm. The byte array is represented by a Unicode-encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initializefromencodedpublickeyinfo">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509publickey-initialize">Initialize</a> method to initialize the public key object before calling this property.

The AlgorithmIdentifier <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) object that is referenced by the SubjectPublicKeyInfo object in an <a href="/windows/desktop/SecGloss/x-gly">X.509</a> version 3 certificate contains an algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and optional parameters.


``` syntax

SubjectPublicKeyInfo  ::=  SEQUENCE
{
   algorithm            AlgorithmIdentifier,
   subjectPublicKey     BIT STRING  
}

AlgorithmIdentifier  ::=  SEQUENCE  
{
   algorithm            OBJECT IDENTIFIER,
   parameters           ANY DEFINED BY algorithm OPTIONAL  
}

```

 The format and content of the parameters differs by algorithm. The <a href="/windows/desktop/SecCrypto/certificate-enrollment-control">Certificate Enrollment Control</a> generates parameter values for various algorithms as required. For more information, see the following sections:<ul>
<li><b>RSA Public Key Algorithm</b></li>
<li><b>Key Transport Using RSA-OAEP</b></li>
<li><b>Key Agreement Using ECDH</b></li>
<li><b>Content Encryption Using AES</b></li>
</ul>


<h3><a id="rsa_public_key_algorithm_cpp"></a><a id="RSA_PUBLIC_KEY_ALGORITHM_CPP"></a>RSA Public Key Algorithm</h3>
 RSA is often used to encrypt a <a href="/windows/desktop/SecGloss/p-gly">private key</a> and send it to a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) for archival. The XCN_OID_RSA_RSA (1.2.840.113549.1.1.1) algorithm OID must have a <b>NULL</b> parameter value. The ASN.1 <b>NULL</b> value is represented by two bytes. The tag number is 0x05 and the value associated with the tag is 0x00. This is shown by the following  certificate example.


``` syntax

...
Public Key Algorithm:
    Algorithm ObjectId: 1.2.840.113549.1.1.1 RSA (RSA_KEYX)
    Algorithm Parameters:
    05 00
...

```

<h3><a id="key_transport_using_rsa-oaep"></a><a id="KEY_TRANSPORT_USING_RSA-OAEP"></a>Key Transport Using RSA-OAEP</h3>
The RSA-OAEP algorithm, XCN_OID_RSAES_OAEP (1.2.840.113549.1.1.7), is also supported for key transport. The parameters field has the following syntax.


``` syntax

RSAES-OAEP-params  ::=  SEQUENCE  
{
   hashFunc    [0] AlgorithmIdentifier DEFAULT sha1OID,
   maskGenFunc [1] AlgorithmIdentifier DEFAULT mgf1SHA1OID,
   pSourceFunc [2] AlgorithmIdentifier DEFAULT pSpecifiedEmptyOID
}

```

<h3><a id="key_agreement_using_ecdh"></a><a id="KEY_AGREEMENT_USING_ECDH"></a>Key Agreement Using ECDH</h3>
The single pass Elliptic Curve Diffie-Hellman algorithm, XCN_OID_DH_SINGLE_PASS_STDDH_SHA1_KDF (1.3.133.16.840.63.0.2), is supported for key agreement. Key agreement uses two levels of encryption:<ul>
<li>The message is encrypted by using a content encryption key (CEK) and a <a href="/windows/desktop/SecGloss/s-gly">symmetric encryption</a> algorithm.</li>
<li>The CEK is encrypted (wrapped) by using a <a href="/windows/desktop/SecGloss/s-gly">symmetric key</a> encryption key (KEK).</li>
</ul>The KEK is computed from a shared secret number that is computed from the private key of one party and the public key of the other party. The parameters field contains the OID of the  KEK algorithm used to wrap or encrypt the CEK. The following wrap algorithms are supported:<ul>
<li>XCN_OID_RSA_SMIMEalgCMS3DESwrap (1.2.840.113549.1.9.16.3.)</li>
<li>XCN_OID_RSA_SMIMEalgCMSRC2wrap (1.2.840.113549.1.9.16.3.7)</li>
<li>XCN_OID_NIST_AES128_WRAP (2.16.840.1.101.3.4.1.5)</li>
<li>XCN_OID_NIST_AES192_WRAP (2.16.840.1.101.3.4.1.25)</li>
<li>XCN_OID_NIST_AES256_WRAP (2.16.840.1.101.3.4.1.45)</li>
</ul>


<h3><a id="content_encryption_using_aes"></a><a id="CONTENT_ENCRYPTION_USING_AES"></a>Content Encryption Using AES</h3>
The Advanced Encryption Standard (AES) is used to encrypt content. The following algorithms are supported:<ul>
<li>XCN_OID_NIST_AES128_CBC        (2.16.840.1.101.3.4.1.2)</li>
<li>XCN_OID_NIST_AES192_CBC        (2.16.840.1.101.3.4.1.22)</li>
<li>XCN_OID_NIST_AES256_CBC        (2.16.840.1.101.3.4.1.42)</li>
</ul>The parameters field contains a random initialization vector, AES-IV.


``` syntax

AES-IV ::= OCTET STRING (SIZE(16))

```


## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a>
