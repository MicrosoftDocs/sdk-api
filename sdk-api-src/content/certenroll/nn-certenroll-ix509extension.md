---
UID: NN:certenroll.IX509Extension
title: IX509Extension
author: windows-sdk-content
description: Can be used to define an extension for a certificate request.
old-location: security\ix509extension.htm
tech.root: SecCertEnroll
ms.assetid: f04e3f63-c826-4401-a1c8-b2614e0dc374
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509Extension, IX509Extension interface [Security], IX509Extension interface [Security],described, certenroll/IX509Extension, security.ix509extension
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
 - IX509Extension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Extension interface


## -description


The <b>IX509Extension</b> interface can be used to define an extension for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. Certificate extensions provide information about key usage, certificate policies and constraints, alternative name forms, and more. An extension consists of an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the extension value as shown by the following <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) syntax.
<pre class="syntax" xml:space="preserve"><code>
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
</code></pre>The Certificate Enrollment API contains the following interfaces, derived from <b>IX509Extension</b>, that you can use to create the various extensions used most commonly in a public key infrastructure (PKI) that relies on a Windows <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate server</a>.<div class="alert"><b>Note</b>  Do not use the <b>IX509Extension</b> base interface to represent any extension that can be represented by one of the following interfaces. Enrollment behavior is undefined if the appropriate interface is not used.</div>
<div> </div>
<table>
<tr>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a>
</td>
<td>Defines an <b>AlternativeNames</b> extension that contains one or more alternative name forms for the subject of the certificate request.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a>
</td>
<td>Defines an <b>AuthorityKeyIdentifier</b> extension that enables identification of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> that corresponds to the certification authority <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> that signed an issued certificate. It is used  by certificate path building software on a Windows server to find the certification authority certificate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/81a1d567-191f-463c-ba67-0867025d8756">IX509ExtensionBasicConstraints</a>
</td>
<td>Defines a <b>BasicConstraints</b> extension that identifies whether the entity can be used as a certification authority and, if so, the number of subordinate certification authorities that can exist beneath it in the certificate chain.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d35d155c-fb81-4d7e-b5c9-82ac5af4b79e">IX509ExtensionCertificatePolicies</a>
</td>
<td>Defines a <b>CertificatePolicies</b> extension that identifies the policies under which the certificate has been issued and the purposes for which it can be used.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/0b9606d0-351c-4d2d-b876-545a9c2cf916">IX509ExtensionEnhancedKeyUsage</a>
</td>
<td>Defines an <b>EnhancedKeyUsage</b> extension that identifies one or more uses of the public key contained in the certificate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4325e6aa-99bb-4c9a-9b19-c5352ebf27b9">IX509ExtensionKeyUsage</a>
</td>
<td>Defines a <b>KeyUsage</b> extension that restricts the operations that can be performed by the public key contained in the certificate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/35b6449e-5a82-4f47-bdda-5356f44bb1fd">IX509ExtensionMSApplicationPolicies</a>
</td>
<td>Defines an <b>MSApplicationPolicies</b> extension that can be used by an application to filter certificates on the basis of permitted use. Permitted uses are identified by object identifiers (OIDs).</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/06dca62d-282b-4bdd-bc8d-4d2e6eb226b5">IX509ExtensionSmimeCapabilities</a>
</td>
<td>Defines an <b>SmimeCapabilities</b> extension that identifies the decryption capabilities of an email recipient so that the sender of the email can choose the most secure encryption algorithm supported by both parties. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/dcf28967-65e0-4669-b1b1-b3d42f1b3d6b">IX509ExtensionSubjectKeyIdentifier</a>
</td>
<td>Defines a <b>SubjectKeyIdentifier</b> extension that differentiates between multiple public keys held by the certificate owner. The extension value is typically a SHA-1 hash of the key.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a>
</td>
<td>Defines a <b>Template</b> extension that identifies the version 2 template to use when issuing or renewing a certificate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9a2d0219-6fe3-4a75-8d28-281c0b863a35">IX509ExtensionTemplateName</a>
</td>
<td>Defines a <b>TemplateName</b> extension that identifies the version 1 template to use when issuing or renewing a certificate.</td>
</tr>
</table>
 



Most of the extensions that can be created by using the preceding  interfaces are defined by the version 3 <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> syntax standard. To create the version 3 extensions for which Microsoft does not provide a custom object, you can use the <b>IX509Extension</b> interface. These extensions are identified in the following table.<table>
<tr>
<th>Extension/OID</th>
<th>Description</th>
</tr>
<tr>
<td><b>AuthorityInformationAccess</b>(XCN_OID_AUTHORITY_INFO_ACCESS)

</td>
<td>Identifies how to access certification authority information and services. The extension value contains a sequence of URIs.</td>
</tr>
<tr>
<td><b>CrlDistributionPoints</b>(XCN_OID_CRL_DIST_POINTS)

</td>
<td>Contains the URI of the base <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL).</td>
</tr>
<tr>
<td><b>FreshestCRL</b>(XCN_OID_FRESHEST_CRL)

</td>
<td>Contains the URI of the delta CRL. The same ASN.1 syntax is used for this extension and the <b>CrlDistributionPoints</b> extension.</td>
</tr>
<tr>
<td><b>NameConstraints</b>(XCN_OID_NAME_CONSTRAINTS)

</td>
<td>Identifies the namespace within which all subject names of certificates in a certificate hierarchy must be located. The extension is used only in a certification authority certificate.</td>
</tr>
<tr>
<td><b>PolicyConstraints</b>(XCN_OID_POLICY_CONSTRAINTS)

</td>
<td>Constrains path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</td>
</tr>
<tr>
<td><b>PolicyMappings</b>(XCN_OID_POLICY_MAPPINGS)

</td>
<td>Identifies the policies in a subordinate certification authority that correspond to policies in the issuing certification authority. The extension value contains a sequence of issuing certification authority and subordinate certification authority policy mappings represented by object identifiers.</td>
</tr>
<tr>
<td><b>PrivateKeyUsagePeriod</b>(XCN_OID_PRIVATEKEY_USAGE_PERIOD)

</td>
<td>Specifies a different validity period for the private key than for the certificate with which the key is associated. </td>
</tr>
<tr>
<td><b>SubjectDirectoryAttributes</b>(XCN_OID_SUBJECT_DIR_ATTRS)

</td>
<td>Conveys identification attributes such as nationality about the certificate subject. The extension value is a sequence of OID-value pairs.</td>
</tr>
</table>
 



Finally, you can use the <b>IX509Extension</b> interface to define private extensions that contain information that is unique to a specific community.

Extensions are added to the <b>Attributes</b> structure of a PKCS #10 request and to the <b>TaggedAttributes</b> structure of a CMC request. To add extensions to either request format, you must first add them to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Extension</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509Extension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509Extension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a01a371b-7dc2-4204-8029-269ac4a9c0d5">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509Extension</b> object from an OID and a byte array that contains the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded extension.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Extension</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that identifies whether the certificate extension is critical.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the OID for the certificate extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/779ad765-e767-4594-afdb-49fe79a8e64b">RawData</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the extension value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/2aefde1b-0f77-4a88-8851-5bacd363900b">ICryptAttribute</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a>



<a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a>
 

 

