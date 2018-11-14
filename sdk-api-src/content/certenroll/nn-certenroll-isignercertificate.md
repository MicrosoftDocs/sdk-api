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
 - ISignerCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISignerCertificate interface


## -description


The <b>ISignerCertificate</b> interface represents a signing <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate</a> that enables you to sign a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a>. When you initialize the interface, the Certificate Enrollment Control retrieves the signing certificate from the personal store and uses it to find an associated <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>. You can use the private key to sign a PKCS #7 or a CMC request but not a PKCS #10 request. PKCS #10 requests must be signed by using the private key associated with the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> included in the request. Self-signed certificates can be signed by using the private key associated with the request or the private key associated with the signing certificate. This is summarized in the following table.<table>
<tr>
<th>Request type (Interface)</th>
<th>Signing certificates</th>
</tr>
<tr>
<td>PKCS #7(<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>)

</td>
<td>1</td>
</tr>
<tr>
<td>PKCS #10(<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10)</a>


</td>
<td>0</td>
</tr>
<tr>
<td>CMC(<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>)

</td>
<td>0 or more</td>
</tr>
<tr>
<td>Self-signed(<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>)

</td>
<td>0 or 1</td>
</tr>
</table>
 



When signing a CMC request, the data to be signed consists of a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded <b>CmcData</b> object wrapped in a CMS <b>SignedData</b> object. The <b>encryptedDigest</b> field of the <b>SignerInfo</b> object contains a signature, and multiple <b>SignerInfo</b> objects can be associated with the request.
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
</code></pre>Each <b>ISignerCertificate</b> object is associated with one <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object that identifies the hashing and public key algorithms used. This object is created and initialized when the <b>ISignerCertificate</b> object is initialized.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISignerCertificate</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISignerCertificate</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa376832(v=VS.85).aspx">Initialize</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa376831(v=VS.85).aspx">Certificate</a>


</td>
<td align="left" width="63%">
Retrieves a DER-encoded byte array that contains the certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376834(v=VS.85).aspx">ParentWindow</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the ID of the window used to display the signing certificate information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376835(v=VS.85).aspx">Pin</a>


</td>
<td align="left" width="63%">
Specifies a personal identification number that authenticates smart card users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376836(v=VS.85).aspx">PrivateKey</a>


</td>
<td align="left" width="63%">
Retrieves the private key associated with the <b>ISignerCertificate</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376838(v=VS.85).aspx">SignatureInformation</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a> object that contains information about the certificate signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376839(v=VS.85).aspx">Silent</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether the user is notified when the private key is used to sign a certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376840(v=VS.85).aspx">UIContextMessage</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains user interface text associated with the  signing certificate.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376821(v=VS.85).aspx">ISignerCertificates</a>
 

 

