---
UID: NN:certenroll.IX509SignatureInformation
title: IX509SignatureInformation
author: windows-sdk-content
description: Represents information used to sign a certificate request.
old-location: security\ix509signatureinformation.htm
tech.root: seccertenroll
ms.assetid: 25774ccb-8e76-443d-89da-177d6e77c019
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509SignatureInformation, IX509SignatureInformation interface [Security], IX509SignatureInformation interface [Security],described, certenroll/IX509SignatureInformation, security.ix509signatureinformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IX509SignatureInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509SignatureInformation interface


## -description


The <b>IX509SignatureInformation</b> interface represents information used to sign a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a>. This includes signature, <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">hash</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key algorithms</a>, and public key parameters. The signature process consists of digesting the certificate request by using a hash algorithm, encoding the digest and the hash algorithm identifier by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER), and signing (encrypting) the result.

The algorithms used in this process can be either discrete or combined. Discrete algorithms are represented by separate <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifiers</a> (OIDs) for the hashing algorithm and the signing algorithm. Discrete algorithms are used when signing a PKCS #7 or CMC request. Examples include the following values.<table>
<tr>
<th>Discrete algorithm OID</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_NIST_sha256(2.16.840.1.101.3.4.2.1)

</td>
<td>National Institute of Standards and Technologies (NIST) 256-bit SHA hashing algorithm.</td>
</tr>
<tr>
<td>XCN_OID_OIWSEC_rsaSign(1.3.14.3.2.11)

</td>
<td>NIST OSE Implementer Workshop Security (OIWSEC) RSA signing algorithm.</td>
</tr>
</table>
 



Combined algorithms, which can be used to sign PKCS #10 requests, are represented by a single OID that identifies both the hashing and the signing algorithm. Examples include the following values.<table>
<tr>
<th>Combined algorithm OID</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_RSA_MD2RSA(1.2.840.113549.1.1.2)

</td>
<td>MD2 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</td>
</tr>
<tr>
<td>XCN_OID_OIWSEC_md5RSA(1.3.14.3.2.3)

</td>
<td>OIWSEC MD5 hashing algorithm combined with the RSA encryption algorithm.</td>
</tr>
</table>
 



The object is automatically initialized when an <a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>, or <a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a> object is initialized.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509SignatureInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509SignatureInformation</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509SignatureInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa379053(v=VS.85).aspx">GetSignatureAlgorithm</a>
</td>
<td align="left" width="63%">
Retrieves the signing algorithm <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa379060(v=VS.85).aspx">SetDefaultValues</a>
</td>
<td align="left" width="63%">
Specifies a default hashing algorithm used to create a digest of the certificate request prior to  signing.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509SignatureInformation</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa965846(v=VS.85).aspx">AlternateSignatureAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that specifies whether the <a href="https://msdn.microsoft.com/en-us/library/Aa379053(v=VS.85).aspx">GetSignatureAlgorithm</a> method should retrieve a discrete or combined algorithm OID for a PKCS #10 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa965845(v=VS.85).aspx">AlternateSignatureAlgorithmSet</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the <a href="https://msdn.microsoft.com/en-us/library/Aa965846(v=VS.85).aspx">AlternateSignatureAlgorithm</a> property has been explicitly set by a caller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa379054(v=VS.85).aspx">HashAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves an OID for the hashing algorithm used in the <a href="https://msdn.microsoft.com/en-us/library/Aa379053(v=VS.85).aspx">GetSignatureAlgorithm</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa379056(v=VS.85).aspx">NullSigned</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that indicates whether the certificate request is null-signed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa379057(v=VS.85).aspx">Parameters</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the parameters associated with the signature algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa379059(v=VS.85).aspx">PublicKeyAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves an OID for the public key algorithm used in the <a href="https://msdn.microsoft.com/en-us/library/Aa379053(v=VS.85).aspx">GetSignatureAlgorithm</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374874(v=VS.85).aspx">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376820(v=VS.85).aspx">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
 

 

