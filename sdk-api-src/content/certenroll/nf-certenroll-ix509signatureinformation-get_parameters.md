---
UID: NF:certenroll.IX509SignatureInformation.get_Parameters
title: IX509SignatureInformation::get_Parameters (certenroll.h)
description: Retrieves a byte array that contains the parameters associated with the signature algorithm. (Get)
helpviewer_keywords: ["IX509SignatureInformation interface [Security]","Parameters property","IX509SignatureInformation.Parameters","IX509SignatureInformation.get_Parameters","IX509SignatureInformation::Parameters","IX509SignatureInformation::get_Parameters","IX509SignatureInformation::put_Parameters","Parameters property [Security]","Parameters property [Security]","IX509SignatureInformation interface","certenroll/IX509SignatureInformation::Parameters","certenroll/IX509SignatureInformation::get_Parameters","certenroll/IX509SignatureInformation::put_Parameters","get_Parameters","security.ix509signatureinformation_parameters_property"]
old-location: security\ix509signatureinformation_parameters_property.htm
tech.root: security
ms.assetid: cb5675d5-cf06-4407-a7fd-b703a56cacba
ms.date: 12/05/2018
ms.keywords: IX509SignatureInformation interface [Security],Parameters property, IX509SignatureInformation.Parameters, IX509SignatureInformation.get_Parameters, IX509SignatureInformation::Parameters, IX509SignatureInformation::get_Parameters, IX509SignatureInformation::put_Parameters, Parameters property [Security], Parameters property [Security],IX509SignatureInformation interface, certenroll/IX509SignatureInformation::Parameters, certenroll/IX509SignatureInformation::get_Parameters, certenroll/IX509SignatureInformation::put_Parameters, get_Parameters, security.ix509signatureinformation_parameters_property
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
 - IX509SignatureInformation::get_Parameters
 - certenroll/IX509SignatureInformation::get_Parameters
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
 - IX509SignatureInformation.Parameters
 - IX509SignatureInformation.get_Parameters
 - IX509SignatureInformation.put_Parameters
---

# IX509SignatureInformation::get_Parameters


## -description

The <b>Parameters</b> property retrieves a byte array that contains the parameters associated with the signature algorithm. The byte array is represented by a Unicode-encoded string.

This property is read/write.

## -parameters

## -remarks

The AlgorithmIdentifier ASN.1 object that is used in various fields of an <a href="/windows/desktop/SecGloss/x-gly">X.509</a> version 3 certificate contains an algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and optional parameters.


``` syntax

AlgorithmIdentifier  ::=  SEQUENCE  
{
   algorithm               OBJECT IDENTIFIER,
   parameters              ANY DEFINED BY algorithm OPTIONAL  
}

```

 The format and content of the parameters differs by algorithm. The Certificate Enrollment Control generates parameter information as required. Parameter values generated for various algorithms are discussed in the following sections.

<b>PKCS #1 version 1.5 signature algorithms:  </b><p class="note"> The following OIDs must have a <b>NULL</b> parameter value. <ul>
<li>XCN_OID_RSA_MD2RSA (1.2.840.113549.1.1.2)</li>
<li>XCN_OID_RSA_MD5RSA (1.2.840.113549.1.1.4)</li>
<li>XCN_OID_RSA_SHA1RSA (1.2.840.113549.1.1.5)</li>
<li>XCN_OID_RSA_SHA256RSA (1.2.840.113549.1.1.11)</li>
<li>XCN_OID_RSA_SHA384RSA (1.2.840.113549.1.1.12)</li>
<li>XCN_OID_RSA_SHA512RSA (1.2.840.113549.1.1.13)</li>
</ul>


<p class="note">The ASN.1 <b>NULL</b> value is represented by two bytes. The tag number is 0x05 and the value associated with the tag, representing the parameter length, is 0x00. This is shown by the following  certificate example.


``` syntax

...
Public Key Algorithm:
    Algorithm ObjectId: 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
    Algorithm Parameters:
    05 00
...

```



<b>RSASSA-PSS signatures:  </b><p class="note">The RSASSA-PSS (RSA Signature Scheme with Appendix - Probabilistic Signature Scheme), XCN_OID_RSA_SSA_PSS (1.2.840.113549.1.1.10), generates the following parameter information. A signature scheme with appendix consists of signature generation and signature verification operations. Verification of the signature requires the original certificate request on which the signature was generated. For more information, see the PKCS #1 v2.1 cryptography standard from RSA laboratories.


``` syntax

RSASSA-PSS-params ::= SEQUENCE 
{
   hashAlgorithm     [0] HashAlgorithm DEFAULT sha1,
   maskGenAlgorithm  [1] MaskGenAlgorithm DEFAULT mgf1SHA1,
   saltLength        [2] INTEGER DEFAULT 20,
   trailerField      [3] TrailerField DEFAULT trailerFieldBC
}


```



<b>ECDSA-SHA1 signature algorithms:  </b>When the XCN_OID_ECDSA_SHA1 (1.2.840.10045.4.1) is used to create a signature, the parameters contains the OID of the hash algorithm. The following OIDs are supported:<ul>
<li>XCN_OID_ECDSA_SHA256 (1.2.840.10045.4.3.2)</li>
<li>XCN_OID_ECDSA_SHA384 (1.2.840.10045.4.3.3)</li>
<li>XCN_OID_ECDSA_SHA512 (1.2.840.10045.4.3.4)</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
