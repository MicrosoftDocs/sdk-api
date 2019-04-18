---
UID: NN:certenroll.IX509CertificateRequestPkcs10
title: IX509CertificateRequestPkcs10 (certenroll.h)
author: windows-sdk-content
description: The IX509CertificateRequestPkcs10 interface represents a PKCS #10 certificate request. The public key cryptography standard (PKCS) #10 defines the format of messages sent to a certification or registration authority to request a public-key certificate.
old-location: security\ix509certificaterequestpkcs10.htm
tech.root: seccertenroll
ms.assetid: 5b3764dc-fc63-45cc-8c35-65539c461e81
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10, IX509CertificateRequestPkcs10 interface [Security], IX509CertificateRequestPkcs10 interface [Security],described, certenroll/IX509CertificateRequestPkcs10, security.ix509certificaterequestpkcs10
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
 - IX509CertificateRequestPkcs10
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509CertificateRequestPkcs10 interface


## -description


The <b>IX509CertificateRequestPkcs10</b> interface represents a PKCS #10 certificate request. The public key cryptography standard (PKCS) #10 defines the format of messages sent to a certification or registration authority to request a public-key certificate.

A PKCS #10 ASN.1 request object contains a version identifier, the subject name, a public key and a set of attributes as shown by the following syntax example.
<pre class="syntax" xml:space="preserve"><code>
--------------------------------------------------------------------
-- Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

-------------------------------------------------------
-- Version number.
-------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

-------------------------------------------------------
-- Subject distinguished name (DN).
-------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               EncodedObjectID,
   value              ANY 
}

-------------------------------------------------------
-- Public key information.
-------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

-------------------------------------------------------
-- Attributes.
-------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               EncodedObjectID,
   values             AttributeSetValue
}</code></pre>The <b>CertificationRequestInfo</b> ASN.1 object is wrapped in a <b>CertificationRequest</b> object as shown by the following syntax. The <b>CertificationRequest</b> object also includes the signature and  the signature algorithm. A PKCS #10 request must be signed by the associated private key or null-signed if it is a cross-certification request. You can call the <a href="https://msdn.microsoft.com/1830a569-03a4-4692-adbf-b627bf4370a1">RawData</a> property to retrieve the signed <b>CertificationRequest</b> object, and you can call the <a href="https://msdn.microsoft.com/43e7e3e2-d94d-46b4-b76b-cd54f9d618ec">RawDataToBeSigned</a> property to retrieve the unsigned <b>CertificationRequestInfo</b> object.
<pre class="syntax" xml:space="preserve"><code>
--------------------------------------------------------------------
-- Certificate request.
--------------------------------------------------------------------
CertificationRequest ::= SEQUENCE 
{
   certificationRequestInfo   CertificationRequestInfo,
   signatureAlgorithm         AlgorithmIdentifier,
   signature                  BIT STRING
}

--------------------------------------------
--  Algorithm Identifier
--------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
   algorithm           EncodedObjectID,
   parameters          ANY OPTIONAL
}
</code></pre>The following properties can be set before calling the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method:<ul>
<li>
<a href="https://msdn.microsoft.com/57a87aab-1e53-4b0b-a7b9-2fe89083819b">AlternateSignatureAlgorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/728dba16-cda8-4eca-8cf0-4e6139e3808b">ClientId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9f68ee54-5dea-47bb-8a90-0285d081c9b8">HashAlgorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/86e82a6c-7689-4bf3-8f64-e512040abd6a">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ab046b65-a059-4b48-a6cd-7e2f0b18bc65">RenewalCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/339c8d47-4406-4f2e-b927-b2dd5f58d1ec">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3a7847b6-52b4-4058-8113-cbc3b9101a5b">SuppressDefaults</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0eedb520-06c3-4106-8593-1c5fb0829d5e">UIContextMessage</a>
</li>
</ul>Also, the <a href="https://msdn.microsoft.com/339c8d47-4406-4f2e-b927-b2dd5f58d1ec">Silent</a>, <a href="https://msdn.microsoft.com/86e82a6c-7689-4bf3-8f64-e512040abd6a">ParentWindow</a>, and <a href="https://msdn.microsoft.com/0eedb520-06c3-4106-8593-1c5fb0829d5e">UIContextMessage</a> properties are typically called before calling an initialization method.

The following properties must be set, if at all, before calling the Encode method:<ul>
<li>
<a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d4a99b08-5616-4c75-b99f-680f55288baa">KeyContainerNamePrefix</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5aa027d7-3c31-4b70-92a5-d15d2c410366">SmimeCapabilities</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b521586-f2fc-4b2f-83ab-79f9b972f9a1">Subject</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestPkcs10</b> interface inherits from <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>. <b>IX509CertificateRequestPkcs10</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509CertificateRequestPkcs10</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ef520d9-f6d4-46fd-8e91-c2113ea8eb20">CheckSignature</a>
</td>
<td align="left" width="63%">
Verifies that the certificate request has been signed and that the signature is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50dc8cc5-21ee-4347-a12a-0d6e62901fbb">GetCspStatuses</a>
</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects that matches the intended key use passed to the function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10ab62c3-9c6f-4e1b-8a86-131d08282d9c">InitializeDecode</a>
</td>
<td align="left" width="63%">
Decodes an existing signed or unsigned PKCS #10 certificate request and uses it to initialize the new PKCS #10 request object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using an existing certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b26e69c4-bfe4-4395-aaf6-bc1d045f59cc">InitializeFromPrivateKey</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using an <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object and, optionally, a template.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a>
</td>
<td align="left" width="63%">
Initializes  a null-signed certificate request by using an <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> object and, optionally, a template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ea746c3-b967-41b4-94ae-7b16b93ca4e4">InitializeFromTemplateName</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using a template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/663ca7dd-f108-46bf-9564-cd2d7ec2bb1f">IsSmartCard</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value that indicates whether any of the cryptographic providers associated with the request object is a smart card provider.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestPkcs10</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7ecde7cb-1a73-4fee-a949-c4bb36e61547">CriticalExtensions</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/f376a33e-005b-4810-9a26-b642236ff7af">IObjectIds</a> collection that identifies the version 3 certificate extensions marked as critical.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/078b6c55-8b56-4075-a8fa-b3230041ded0">CryptAttributes</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/beedb57c-1c89-4d16-8514-046e3071fd1e">ICryptAttributes</a> collection of optional certificate attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cad6d8f0-f7d6-4ede-96a2-b00159962a1b">CspStatuses</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects that matches the intended use of the private key associated with the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d4a99b08-5616-4c75-b99f-680f55288baa">KeyContainerNamePrefix</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a prefix used to create the container name for a new private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2420f5ef-2cd7-498d-892a-2b99c524d629">NullSigned</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that indicates whether the certificate request is null-signed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8bb15b5c-e642-477d-bcec-772748e336ef">OldCertificate</a>


</td>
<td align="left" width="63%">
Retrieves the certificate passed to the <a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/691e136f-1434-4b72-b571-e14ade4f2cf2">PrivateKey</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> object that contains the private key used to sign the certificate request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9f9d05d8-9bc5-441e-8409-498ee9d20c25">PublicKey</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> object that contains the public key included in the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/43e7e3e2-d94d-46b4-b76b-cd54f9d618ec">RawDataToBeSigned</a>


</td>
<td align="left" width="63%">
Retrieves  the unsigned certificate request created by the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b6788885-1036-4edd-bbb9-4d9808771d95">ReuseKey</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that indicates whether an existing private key was used to sign the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ee6ad3c7-2d31-4a12-ad37-ee6e1071b665">Signature</a>


</td>
<td align="left" width="63%">
Retrieves the request signature created by the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d90a8b82-a4d7-4d31-bcd0-293572a2bdd2">SignatureInformation</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a> object that contains information about the certificate request signature.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5aa027d7-3c31-4b70-92a5-d15d2c410366">SmimeCapabilities</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that tells the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method whether to create an <a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a> collection that  identifies the encryption capabilities supported by the computer.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7b521586-f2fc-4b2f-83ab-79f9b972f9a1">Subject</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the X.500 distinguished name of the entity requesting the certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f7a6d23-00d3-4ab6-817a-a37490f0cb84">SuppressOids</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the default extension and attribute object identifiers that were not added  to the request when the request was encoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/490a34bc-08b3-4df2-8996-6137bea53420">TemplateObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the   object identifier of the template used to create the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b5500c94-7d7a-473d-80ef-c0d713dcb52e">X509Extensions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the extensions included in the certificate request.

[WebEnabled]

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>
 

 

