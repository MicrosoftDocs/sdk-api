---
UID: NN:certenroll.IX509Extension
title: IX509Extension
author: windows-sdk-content
description: Can be used to define an extension for a certificate request.
old-location: security\ix509extension.htm
tech.root: SecCertEnroll
ms.assetid: f04e3f63-c826-4401-a1c8-b2614e0dc374
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509Extension, IX509Extension interface [Security], IX509Extension interface [Security],described, certenroll/IX509Extension, security.ix509extension
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
 - IX509Extension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Extension interface


## -description


The <b>IX509Extension</b> interface can be used to define an extension for a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a>. Certificate extensions provide information about key usage, certificate policies and constraints, alternative name forms, and more. An extension consists of an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the extension value as shown by the following <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) syntax.
<pre class="syntax" xml:space="preserve"><code>
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
</code></pre>The Certificate Enrollment API contains the following interfaces, derived from <b>IX509Extension</b>, that you can use to create the various extensions used most commonly in a public key infrastructure (PKI) that relies on a Windows <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate server</a>.<div class="alert"><b>Note</b>  Do not use the <b>IX509Extension</b> base interface to represent any extension that can be represented by one of the following interfaces. Enrollment behavior is undefined if the appropriate interface is not used.</div>
<div> </div>
<table>
<tr>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378081(v=VS.85).aspx">IX509ExtensionAlternativeNames</a>
</td>
<td>Defines an <b>AlternativeNames</b> extension that contains one or more alternative name forms for the subject of the certificate request.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378098(v=VS.85).aspx">IX509ExtensionAuthorityKeyIdentifier</a>
</td>
<td>Defines an <b>AuthorityKeyIdentifier</b> extension that enables identification of the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a> that corresponds to the certification authority <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> that signed an issued certificate. It is used  by certificate path building software on a Windows server to find the certification authority certificate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378108(v=VS.85).aspx">IX509ExtensionBasicConstraints</a>
</td>
<td>Defines a <b>BasicConstraints</b> extension that identifies whether the entity can be used as a certification authority and, if so, the number of subordinate certification authorities that can exist beneath it in the certificate chain.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378121(v=VS.85).aspx">IX509ExtensionCertificatePolicies</a>
</td>
<td>Defines a <b>CertificatePolicies</b> extension that identifies the policies under which the certificate has been issued and the purposes for which it can be used.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378132(v=VS.85).aspx">IX509ExtensionEnhancedKeyUsage</a>
</td>
<td>Defines an <b>EnhancedKeyUsage</b> extension that identifies one or more uses of the public key contained in the certificate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378144(v=VS.85).aspx">IX509ExtensionKeyUsage</a>
</td>
<td>Defines a <b>KeyUsage</b> extension that restricts the operations that can be performed by the public key contained in the certificate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378155(v=VS.85).aspx">IX509ExtensionMSApplicationPolicies</a>
</td>
<td>Defines an <b>MSApplicationPolicies</b> extension that can be used by an application to filter certificates on the basis of permitted use. Permitted uses are identified by object identifiers (OIDs).</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378177(v=VS.85).aspx">IX509ExtensionSmimeCapabilities</a>
</td>
<td>Defines an <b>SmimeCapabilities</b> extension that identifies the decryption capabilities of an email recipient so that the sender of the email can choose the most secure encryption algorithm supported by both parties. </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378215(v=VS.85).aspx">IX509ExtensionSubjectKeyIdentifier</a>
</td>
<td>Defines a <b>SubjectKeyIdentifier</b> extension that differentiates between multiple public keys held by the certificate owner. The extension value is typically a SHA-1 hash of the key.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a>
</td>
<td>Defines a <b>Template</b> extension that identifies the version 2 template to use when issuing or renewing a certificate.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Aa378276(v=VS.85).aspx">IX509ExtensionTemplateName</a>
</td>
<td>Defines a <b>TemplateName</b> extension that identifies the version 1 template to use when issuing or renewing a certificate.</td>
</tr>
</table>
 



Most of the extensions that can be created by using the preceding  interfaces are defined by the version 3 <a href="https://msdn.microsoft.com/en-us/library/ms721636(v=VS.85).aspx">X.509</a> syntax standard. To create the version 3 extensions for which Microsoft does not provide a custom object, you can use the <b>IX509Extension</b> interface. These extensions are identified in the following table.<table>
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
<td>Contains the URI of the base <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation list</a> (CRL).</td>
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

Extensions are added to the <b>Attributes</b> structure of a PKCS #10 request and to the <b>TaggedAttributes</b> structure of a CMC request. To add extensions to either request format, you must first add them to an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa379077(v=VS.85).aspx">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/en-us/library/Aa374900(v=VS.85).aspx">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509Extension</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509Extension</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa378511(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an <b>IX509Extension</b> object from an OID and a byte array that contains the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded extension.

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

<a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that identifies whether the certificate extension is critical.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the OID for the certificate extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378524(v=VS.85).aspx">RawData</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the extension value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374874(v=VS.85).aspx">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375929(v=VS.85).aspx">ICryptAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a>
 

 

