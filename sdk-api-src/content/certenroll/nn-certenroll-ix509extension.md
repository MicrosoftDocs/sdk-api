---
UID: NN:certenroll.IX509Extension
title: IX509Extension (certenroll.h)
description: Can be used to define an extension for a certificate request.
helpviewer_keywords: ["IX509Extension","IX509Extension interface [Security]","IX509Extension interface [Security]","described","certenroll/IX509Extension","security.ix509extension"]
old-location: security\ix509extension.htm
tech.root: security
ms.assetid: f04e3f63-c826-4401-a1c8-b2614e0dc374
ms.date: 12/05/2018
ms.keywords: IX509Extension, IX509Extension interface [Security], IX509Extension interface [Security],described, certenroll/IX509Extension, security.ix509extension
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
 - IX509Extension
 - certenroll/IX509Extension
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
 - IX509Extension
---

# IX509Extension interface


## -description

The <b>IX509Extension</b> interface can be used to define an extension for a <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. Certificate extensions provide information about key usage, certificate policies and constraints, alternative name forms, and more. An extension consists of an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the extension value as shown by the following <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) syntax.

``` syntax

Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}

```
The Certificate Enrollment API contains the following interfaces, derived from <b>IX509Extension</b>, that you can use to create the various extensions used most commonly in a public key infrastructure (PKI) that relies on a Windows <a href="/windows/desktop/SecGloss/c-gly">certificate server</a>.<div class="alert"><b>Note</b>  Do not use the <b>IX509Extension</b> base interface to represent any extension that can be represented by one of the following interfaces. Enrollment behavior is undefined if the appropriate interface is not used.</div>
<div> </div>
<table>
<tr>
<th>Interface</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a>
</td>
<td>Defines an <b>AlternativeNames</b> extension that contains one or more alternative name forms for the subject of the certificate request.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionauthoritykeyidentifier">IX509ExtensionAuthorityKeyIdentifier</a>
</td>
<td>Defines an <b>AuthorityKeyIdentifier</b> extension that enables identification of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> <a href="/windows/desktop/SecGloss/p-gly">public key</a> that corresponds to the certification authority <a href="/windows/desktop/SecGloss/p-gly">private key</a> that signed an issued certificate. It is used  by certificate path building software on a Windows server to find the certification authority certificate.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionbasicconstraints">IX509ExtensionBasicConstraints</a>
</td>
<td>Defines a <b>BasicConstraints</b> extension that identifies whether the entity can be used as a certification authority and, if so, the number of subordinate certification authorities that can exist beneath it in the certificate chain.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a>
</td>
<td>Defines a <b>CertificatePolicies</b> extension that identifies the policies under which the certificate has been issued and the purposes for which it can be used.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a>
</td>
<td>Defines an <b>EnhancedKeyUsage</b> extension that identifies one or more uses of the public key contained in the certificate.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a>
</td>
<td>Defines a <b>KeyUsage</b> extension that restricts the operations that can be performed by the public key contained in the certificate.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionmsapplicationpolicies">IX509ExtensionMSApplicationPolicies</a>
</td>
<td>Defines an <b>MSApplicationPolicies</b> extension that can be used by an application to filter certificates on the basis of permitted use. Permitted uses are identified by object identifiers (OIDs).</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a>
</td>
<td>Defines an <b>SmimeCapabilities</b> extension that identifies the decryption capabilities of an email recipient so that the sender of the email can choose the most secure encryption algorithm supported by both parties. </td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a>
</td>
<td>Defines a <b>SubjectKeyIdentifier</b> extension that differentiates between multiple public keys held by the certificate owner. The extension value is typically a SHA-1 hash of the key.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>
</td>
<td>Defines a <b>Template</b> extension that identifies the version 2 template to use when issuing or renewing a certificate.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a>
</td>
<td>Defines a <b>TemplateName</b> extension that identifies the version 1 template to use when issuing or renewing a certificate.</td>
</tr>
</table>
 



Most of the extensions that can be created by using the preceding  interfaces are defined by the version 3 <a href="/windows/desktop/SecGloss/x-gly">X.509</a> syntax standard. To create the version 3 extensions for which Microsoft does not provide a custom object, you can use the <b>IX509Extension</b> interface. These extensions are identified in the following table.<table>
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
<td>Contains the URI of the base <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).</td>
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

Extensions are added to the <b>Attributes</b> structure of a PKCS #10 request and to the <b>TaggedAttributes</b> structure of a CMC request. To add extensions to either request format, you must first add them to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509Extension</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509Extension</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattribute">ICryptAttribute</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a>
