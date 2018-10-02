---
UID: NN:certenroll.ISignerCertificate
title: ISignerCertificate
author: windows-sdk-content
description: Represents a signing certificate that enables you to sign a certificate request.
old-location: security\isignercertificate.htm
tech.root: SecCertEnroll
ms.assetid: 146a1925-4de6-492c-8014-612c65bd7270
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISignerCertificate, ISignerCertificate interface [Security], ISignerCertificate interface [Security],described, certenroll/ISignerCertificate, security.isignercertificate
ms.prod: windows
ms.technology: windows-sdk
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
 - ISignerCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISignerCertificate interface


## -description


The <b>ISignerCertificate</b> interface represents a signing <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> that enables you to sign a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. When you initialize the interface, the Certificate Enrollment Control retrieves the signing certificate from the personal store and uses it to find an associated <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. You can use the private key to sign a PKCS #7 or a CMC request but not a PKCS #10 request. PKCS #10 requests must be signed by using the private key associated with the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> included in the request. Self-signed certificates can be signed by using the private key associated with the request or the private key associated with the signing certificate. This is summarized in the following table.<table>
<tr>
<th>Request type (Interface)</th>
<th>Signing certificates</th>
</tr>
<tr>
<td>PKCS #7(<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>)

</td>
<td>1</td>
</tr>
<tr>
<td>PKCS #10(<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10)</a>


</td>
<td>0</td>
</tr>
<tr>
<td>CMC(<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>)

</td>
<td>0 or more</td>
</tr>
<tr>
<td>Self-signed(<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>)

</td>
<td>0 or 1</td>
</tr>
</table>
 



When signing a CMC request, the data to be signed consists of a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded <b>CmcData</b> object wrapped in a CMS <b>SignedData</b> object. The <b>encryptedDigest</b> field of the <b>SignerInfo</b> object contains a signature, and multiple <b>SignerInfo</b> objects can be associated with the request.
<pre class="syntax" xml:space="preserve"><code>
---------------------------------------------------------------------
-- CMC request data
---------------------------------------------------------------------

CmcData ::= SEQUENCE 
{
controlSequence     SEQUENCE OF TaggedAttribute,
reqSequence         SEQUENCE OF TaggedRequest,
cmsSequence         SEQUENCE OF TaggedContentInfo,
otherMsgSequence    SEQUENCE OF TaggedOtherMs
}

---------------------------------------------------------------------
-- SignedData object that wraps the CMC request
---------------------------------------------------------------------

SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

DigestAlgorithmIdentifiers ::=  SET OF DigestAlgorithmIdentifier 
DigestAlgorithmIdentifiersNC ::= SET OF DigestAlgorithmIdentifierNC

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes OPTIONAL
}
</code></pre>Each <b>ISignerCertificate</b> object is associated with one <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object that identifies the hashing and public key algorithms used. This object is created and initialized when the <b>ISignerCertificate</b> object is initialized.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISignerCertificate</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISignerCertificate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISignerCertificate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2553f0bc-a177-49fc-932f-080cb4bd7a5c">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a signing certificate.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISignerCertificate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7c7cc326-593d-4b2b-b8db-46aaf894279b">Certificate</a>


</td>
<td align="left" width="63%">
Retrieves a DER-encoded byte array that contains the certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a1749c92-11e4-4726-a355-ccdd245b4df8">ParentWindow</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the ID of the window used to display the signing certificate information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/695d895e-0646-4a2e-a699-86674f919bad">Pin</a>


</td>
<td align="left" width="63%">
Specifies a personal identification number that authenticates smart card users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/047a22ba-9817-45b7-aa9a-356245d2b824">PrivateKey</a>


</td>
<td align="left" width="63%">
Retrieves the private key associated with the <b>ISignerCertificate</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e870e17f-42e4-4548-b876-f5e0556bff0e">SignatureInformation</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object that contains information about the certificate signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b598d4a2-d53a-4091-a059-f9674acf9318">Silent</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether the user is notified when the private key is used to sign a certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0fd874b0-9093-4c1b-94a0-a2aaad19010e">UIContextMessage</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains user interface text associated with the  signing certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/420d6550-514a-4fea-987b-6deecbc9b717">ISignerCertificates</a>
 

 

