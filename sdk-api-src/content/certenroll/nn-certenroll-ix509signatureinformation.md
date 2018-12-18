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


The <b>IX509SignatureInformation</b> interface represents information used to sign a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This includes signature, <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a>, and <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithms</a>, and public key parameters. The signature process consists of digesting the certificate request by using a hash algorithm, encoding the digest and the hash algorithm identifier by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER), and signing (encrypting) the result.

The algorithms used in this process can be either discrete or combined. Discrete algorithms are represented by separate <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) for the hashing algorithm and the signing algorithm. Discrete algorithms are used when signing a PKCS #7 or CMC request. Examples include the following values.<table>
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
 



The object is automatically initialized when an <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>, <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>, or <a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a> object is initialized.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509SignatureInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509SignatureInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a>
</td>
<td align="left" width="63%">
Retrieves the signing algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/123e65e8-62bb-4bc7-9e15-113780be81e3">SetDefaultValues</a>
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

<a href="https://msdn.microsoft.com/e62ecdf1-56d8-4707-8e5d-deef4d79a34c">AlternateSignatureAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that specifies whether the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method should retrieve a discrete or combined algorithm OID for a PKCS #10 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fd28072f-9b79-4068-b4dd-61a6a4f8beda">AlternateSignatureAlgorithmSet</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the <a href="https://msdn.microsoft.com/e62ecdf1-56d8-4707-8e5d-deef4d79a34c">AlternateSignatureAlgorithm</a> property has been explicitly set by a caller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b5242975-50e5-49d6-be1f-3a09ada03593">HashAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves an OID for the hashing algorithm used in the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a693343e-7c9a-4967-b46c-53936497662a">NullSigned</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that indicates whether the certificate request is null-signed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cb5675d5-cf06-4407-a7fd-b703a56cacba">Parameters</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the parameters associated with the signature algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f964328f-15a6-4d8e-a2cf-73c8d74995e8">PublicKeyAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves an OID for the public key algorithm used in the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

