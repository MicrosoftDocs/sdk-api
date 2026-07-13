---
UID: NN:certenroll.IX509PublicKey
title: IX509PublicKey (certenroll.h)
description: Represents a public key in a public/private key pair.
helpviewer_keywords: ["IX509PublicKey","IX509PublicKey interface [Security]","IX509PublicKey interface [Security]","described","certenroll/IX509PublicKey","security.ix509publickey"]
old-location: security\ix509publickey.htm
tech.root: security
ms.assetid: cd6f28a3-9998-40d7-a3e8-dab0cf3991a8
ms.date: 12/05/2018
ms.keywords: IX509PublicKey, IX509PublicKey interface [Security], IX509PublicKey interface [Security],described, certenroll/IX509PublicKey, security.ix509publickey
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
 - IX509PublicKey
 - certenroll/IX509PublicKey
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
 - IX509PublicKey
---

# IX509PublicKey interface


## -description

The <b>IX509PublicKey</b> interface represents a   public key in a <a href="/windows/desktop/SecGloss/p-gly">public/private key pair</a>. The public key is included in the certificate request sent to a certification authority (CA) and in the certificate received from the CA. For more information, see <a href="/windows/desktop/SecCrypto/public-private-key-pairs">Public/Private Key Pairs</a>.

The Certificate Enrollment Control passes public and private keys in byte arrays. The following certificate example shows a 1024-bit public key created by using the RSA signing algorithm, XCN_OID_RSA_RSA (1.2.840.113549.1.1.1).

``` syntax

...
Public Key Algorithm:
    Algorithm ObjectId: 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
    Algorithm Parameters:
    05 00
Public Key Length: 1024 bits
Public Key: UnusedBits = 0
    0000  30 81 89 02 81 81 00 8f  e2 41 2a 08 e8 51 a8 8c
    0010  b3 e8 53 e7 d5 49 50 b3  27 8a 2b cb ea b5 42 73
    0020  ea 02 57 cc 65 33 ee 88  20 61 a1 17 56 c1 24 18
    0030  e3 a8 08 d3 be d9 31 f3  37 0b 94 b8 cc 43 08 0b
    0040  70 24 f7 9c b1 8d 5d d6  6d 82 d0 54 09 84 f8 9f
    0050  97 01 75 05 9c 89 d4 d5  c9 1e c9 13 d7 2a 6b 30
    0060  91 19 d6 d4 42 e0 c4 9d  7c 92 71 e1 b2 2f 5c 8d
    0070  ee f0 f1 17 1e d2 5f 31  5b b1 9c bc 20 55 bf 3a
    0080  37 42 45 75 dc 90 65 02  03 01 00 01
...

```
The public key consists of a 1024-bit modulus created by multiplying two large prime numbers and a 96-bit exponent. The RSA algorithm uses the exponent and the prime numbers in the standard Euclidian formula to create a private key. The modulus and exponent can be more clearly identified by examining the following ASN.1 output of the same public key. Because the modulus begins with a byte (0x8F) for which the sign bit is set, 0x00 is prepended to ensure that the integer  remains unsigned. Other public key algorithms create public keys that are made up from different constituent parts.

``` syntax

30 81 89                                  ; SEQUENCE (89 Bytes)
   02 81 81                               ; INTEGER (81 Bytes)
   |  00                                 // Modulus 
   |  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
   |  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
   |  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
   |  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
   |  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
   |  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
   |  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
   |  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
   02 03                                  ; INTEGER (3 Bytes)
      01 00 01                           // Exponent


```


## -inheritance

The <b>IX509PublicKey</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509PublicKey</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>



<a href="/windows/desktop/SecCrypto/public-private-key-pairs">Public/Private Key Pairs</a>
