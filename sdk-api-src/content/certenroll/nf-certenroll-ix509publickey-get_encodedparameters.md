---
UID: NF:certenroll.IX509PublicKey.get_EncodedParameters
title: IX509PublicKey::get_EncodedParameters
author: windows-sdk-content
description: Retrieves a byte array that contains the parameters associated with the public key algorithm.
old-location: security\ix509publickey_encodedparameters_property.htm
tech.root: seccertenroll
ms.assetid: f7c7bf0a-0b66-4676-9448-f74937823f90
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EncodedParameters property [Security], EncodedParameters property [Security],IX509PublicKey interface, IX509PublicKey interface [Security],EncodedParameters property, IX509PublicKey.EncodedParameters, IX509PublicKey.get_EncodedParameters, IX509PublicKey::EncodedParameters, IX509PublicKey::get_EncodedParameters, certenroll/IX509PublicKey::EncodedParameters, certenroll/IX509PublicKey::get_EncodedParameters, get_EncodedParameters, security.ix509publickey_encodedparameters_property
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PublicKey::get_EncodedParameters


## -description


The <b>EncodedParameters</b> property retrieves a byte array that contains the parameters associated with the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> algorithm. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/3e92d934-1ab7-4f09-a579-0dde4ef44c7f">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="https://msdn.microsoft.com/b6db46b2-95f5-4ba9-829d-97bf83fd9806">Initialize</a> method to initialize the public key object before calling this property.

The AlgorithmIdentifier <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) object that is referenced by the SubjectPublicKeyInfo object in an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> version 3 certificate contains an algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and optional parameters.

<pre class="syntax" xml:space="preserve"><code>
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
</code></pre>
 The format and content of the parameters differs by algorithm. The <a href="https://msdn.microsoft.com/ce6661b0-7ed2-452f-a54c-6705d14f3298">Certificate Enrollment Control</a> generates parameter values for various algorithms as required. For more information, see the following sections:<ul>
<li><b>RSA Public Key Algorithm</b></li>
<li><b>Key Transport Using RSA-OAEP</b></li>
<li><b>Key Agreement Using ECDH</b></li>
<li><b>Content Encryption Using AES</b></li>
</ul>


<h3><a id="rsa_public_key_algorithm_cpp"></a><a id="RSA_PUBLIC_KEY_ALGORITHM_CPP"></a>RSA Public Key Algorithm</h3>
 RSA is often used to encrypt a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> and send it to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) for archival. The XCN_OID_RSA_RSA (1.2.840.113549.1.1.1) algorithm OID must have a <b>NULL</b> parameter value. The ASN.1 <b>NULL</b> value is represented by two bytes. The tag number is 0x05 and the value associated with the tag is 0x00. This is shown by the following  certificate example.

<pre class="syntax" xml:space="preserve"><code>
...
Public Key Algorithm:
    Algorithm ObjectId: 1.2.840.113549.1.1.1 RSA (RSA_KEYX)
    Algorithm Parameters:
    05 00
...
</code></pre>
<h3><a id="key_transport_using_rsa-oaep"></a><a id="KEY_TRANSPORT_USING_RSA-OAEP"></a>Key Transport Using RSA-OAEP</h3>
The RSA-OAEP algorithm, XCN_OID_RSAES_OAEP (1.2.840.113549.1.1.7), is also supported for key transport. The parameters field has the following syntax.

<pre class="syntax" xml:space="preserve"><code>
RSAES-OAEP-params  ::=  SEQUENCE  
{
   hashFunc    [0] AlgorithmIdentifier DEFAULT sha1OID,
   maskGenFunc [1] AlgorithmIdentifier DEFAULT mgf1SHA1OID,
   pSourceFunc [2] AlgorithmIdentifier DEFAULT pSpecifiedEmptyOID
}
</code></pre>
<h3><a id="key_agreement_using_ecdh"></a><a id="KEY_AGREEMENT_USING_ECDH"></a>Key Agreement Using ECDH</h3>
The single pass Elliptic Curve Diffie-Hellman algorithm, XCN_OID_DH_SINGLE_PASS_STDDH_SHA1_KDF (1.3.133.16.840.63.0.2), is supported for key agreement. Key agreement uses two levels of encryption:<ul>
<li>The message is encrypted by using a content encryption key (CEK) and a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric encryption</a> algorithm.</li>
<li>The CEK is encrypted (wrapped) by using a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a> encryption key (KEK).</li>
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

<pre class="syntax" xml:space="preserve"><code>
AES-IV ::= OCTET STRING (SIZE(16))
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a>
 

 

