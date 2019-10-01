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
f1_keywords: 
 - "certenroll/IX509CertificateRequestPkcs10"
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
}</code></pre>The <b>CertificationRequestInfo</b> ASN.1 object is wrapped in a <b>CertificationRequest</b> object as shown by the following syntax. The <b>CertificationRequest</b> object also includes the signature and  the signature algorithm. A PKCS #10 request must be signed by the associated private key or null-signed if it is a cross-certification request. You can call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_rawdata">RawData</a> property to retrieve the signed <b>CertificationRequest</b> object, and you can call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_rawdatatobesigned">RawDataToBeSigned</a> property to retrieve the unsigned <b>CertificationRequestInfo</b> object.
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
</code></pre>The following properties can be set before calling the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_clientid">ClientId</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_hashalgorithm">HashAlgorithm</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_parentwindow">ParentWindow</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_renewalcertificate">RenewalCertificate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_silent">Silent</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_suppressdefaults">SuppressDefaults</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>Also, the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_silent">Silent</a>, <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_parentwindow">ParentWindow</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_uicontextmessage">UIContextMessage</a> properties are typically called before calling an initialization method.

The following properties must be set, if at all, before calling the Encode method:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_cspinformations">CspInformations</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_keycontainernameprefix">KeyContainerNamePrefix</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities">SmimeCapabilities</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_subject">Subject</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequestPkcs10</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>. <b>IX509CertificateRequestPkcs10</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-checksignature">CheckSignature</a>
</td>
<td align="left" width="63%">
Verifies that the certificate request has been signed and that the signature is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-getcspstatuses">GetCspStatuses</a>
</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects that matches the intended key use passed to the function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Decodes an existing signed or unsigned PKCS #10 certificate request and uses it to initialize the new PKCS #10 request object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using an existing certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object and, optionally, a template.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</td>
<td align="left" width="63%">
Initializes  a null-signed certificate request by using an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a> object and, optionally, a template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</td>
<td align="left" width="63%">
Initializes the certificate request by using a template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-issmartcard">IsSmartCard</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_criticalextensions">CriticalExtensions</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection that identifies the version 3 certificate extensions marked as critical.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_cryptattributes">CryptAttributes</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection of optional certificate attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_cspstatuses">CspStatuses</a>


</td>
<td align="left" width="63%">
Retrieves a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects that matches the intended use of the private key associated with the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_keycontainernameprefix">KeyContainerNamePrefix</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a prefix used to create the container name for a new private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_nullsigned">NullSigned</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that indicates whether the certificate request is null-signed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_oldcertificate">OldCertificate</a>


</td>
<td align="left" width="63%">
Retrieves the certificate passed to the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_privatekey">PrivateKey</a>


</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> object that contains the private key used to sign the certificate request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_publickey">PublicKey</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a> object that contains the public key included in the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_rawdatatobesigned">RawDataToBeSigned</a>


</td>
<td align="left" width="63%">
Retrieves  the unsigned certificate request created by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_reusekey">ReuseKey</a>


</td>
<td align="left" width="63%">
Retrieves a Boolean value that indicates whether an existing private key was used to sign the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_signature">Signature</a>


</td>
<td align="left" width="63%">
Retrieves the request signature created by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation">SignatureInformation</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object that contains information about the certificate request signature.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_smimecapabilities">SmimeCapabilities</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that tells the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method whether to create an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a> collection that  identifies the encryption capabilities supported by the computer.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_subject">Subject</a>


</td>
<td align="left" width="63%">
Specifies or retrieves the X.500 distinguished name of the entity requesting the certificate.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_suppressoids">SuppressOids</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the default extension and attribute object identifiers that were not added  to the request when the request was encoded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_templateobjectid">TemplateObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the   object identifier of the template used to create the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions">X509Extensions</a>


</td>
<td align="left" width="63%">
Retrieves a collection of the extensions included in the certificate request.

[WebEnabled]

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>
 

 

