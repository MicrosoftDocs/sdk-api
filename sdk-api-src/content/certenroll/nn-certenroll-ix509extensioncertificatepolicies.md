---
UID: NN:certenroll.IX509ExtensionCertificatePolicies
title: IX509ExtensionCertificatePolicies (certenroll.h)
description: Enables you to specify a collection of policy information terms, each of which consists of an object identifier (OID) and optional policy qualifiers. A single policy term is defined by an ICertificatePolicy object.
helpviewer_keywords: ["IX509ExtensionCertificatePolicies","IX509ExtensionCertificatePolicies interface [Security]","IX509ExtensionCertificatePolicies interface [Security]","described","certenroll/IX509ExtensionCertificatePolicies","security.ix509extensioncertificatepolicies"]
old-location: security\ix509extensioncertificatepolicies.htm
tech.root: security
ms.assetid: d35d155c-fb81-4d7e-b5c9-82ac5af4b79e
ms.date: 12/05/2018
ms.keywords: IX509ExtensionCertificatePolicies, IX509ExtensionCertificatePolicies interface [Security], IX509ExtensionCertificatePolicies interface [Security],described, certenroll/IX509ExtensionCertificatePolicies, security.ix509extensioncertificatepolicies
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
 - IX509ExtensionCertificatePolicies
 - certenroll/IX509ExtensionCertificatePolicies
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
 - IX509ExtensionCertificatePolicies
---

# IX509ExtensionCertificatePolicies interface


## -description

The <b>IX509ExtensionCertificatePolicies</b> interface enables you to specify a collection of policy information terms, each of which consists of an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and optional policy qualifiers. A single policy term is defined by an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a> object. The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>.

``` syntax

----------------------------------------------------------------------
-- CertificatePolicies
-- XCN_OID_CERT_POLICIES (2.5.29.32)
----------------------------------------------------------------------

CertificatePolicies ::= SEQUENCE OF PolicyInformation

PolicyInformation ::= SEQUENCE 
{
   policyIdentifier    EncodedObjectID,
   policyQualifiers    PolicyQualifiers OPTIONAL
}

PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   EncodedObjectID,
   qualifier           NOCOPYANY OPTIONAL
}


----------------------------------------------------------------------
-- UserNotice qualifier
-- XCN_OID_PKIX_POLICY_QUALIFIER_USERNOTICE (1.3.6.1.5.5.7.2.2)
----------------------------------------------------------------------

UserNotice ::= SEQUENCE 
{
   noticeRef,      -- Not supported
   explicitText    -- Not supported
}

----------------------------------------------------------------------
-- Certification Practice Statement (CPS) qualifier
-- XCN_OID_PKIX_POLICY_QUALIFIER_CPS (1.3.6.1.5.5.7.2.1)
----------------------------------------------------------------------

CpsURLs ::= SEQUENCE OF SEQUENCE 
{
   url                 IA5String,
   digestAlgorithmId,  -- Not supported
   digest              -- Not supported
}

----------------------------------------------------------------------
-- CertificatePolicies95, XCN_OID_CERT_POLICIES_95 (2.5.29.3),
-- supports the deprecated definition of policies and qualifiers.
----------------------------------------------------------------------

CertificatePolicies95 ::= SEQUENCE OF PolicyQualifiers
    

```
When included in a certificate issued to an end entity, this extension identifies the policies under which the certificate was issued and the purposes for which the certificate can be used. Applications that have specific policy requirements should compare these to the collection of policy <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) in the certificate.

When included in a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> certificate, this extension limits the set of policies for the certification paths extending from the certification authority certificate. If a certification authority does not want to limit this set, it can assert <b>XCN_OID_ANY_CERT_POLICY</b> (2.5.29.32.0).

This extension is supported on Windows Server 2003 and later  certification authorities. The following policies are predefined. The <i>x.y.z</i> portion of each OID represents a randomly generated numeric sequence that is unique for each forest. You can also create custom OIDs to represent custom issuance policies.<table>
<tr>
<th>Policy</th>
<th>Description</th>
</tr>
<tr>
<td>All Issuance(2.5.29.32.0)

</td>
<td>Contains all other policies. This is typically assigned only to certification authority certificates. The OID is XCN_OID_ANY_CERT_POLICY.</td>
</tr>
<tr>
<td>Low Assurance(1.3.6.1.4.1.311.21.8.x.y.z.1.400)

</td>
<td>Indicates that a  certificate is issued with no additional security requirements. </td>
</tr>
<tr>
<td>Medium Assurance (1.3.6.1.4.1.311.21.8.x.y.z.1.401)

</td>
<td>Indicates that a certificate issuance has  additional security requirements. For example, the policy might require that the certificate subject  physically appear before the certification authority.</td>
</tr>
<tr>
<td>High Assurance (1.3.6.1.4.1.311.21.8.x.y.z.1.402)

</td>
<td>Indicates that the certificate is issued with the highest security. For example, the issuance of a key recovery agent certificate can require additional background checks and a digital signature from a designated approver because a person holding this certificate can recover <a href="/windows/desktop/SecGloss/p-gly">private key</a> material from the certification authority.</td>
</tr>
</table>
 



 Policy qualifiers can be used when an OID is considered insufficient to fully identify a policy. Qualifiers are defined by using the <a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a> interface and can be associated with a policy by adding qualifiers to the <a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifiers">IPolicyQualifiers</a> collection retrieved from an  <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a> object. A Windows certification authority supports the following qualifiers.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_PKIX_POLICY_QUALIFIER_USERNOTICE(1.3.6.1.5.5.7.2.2)

</td>
<td>Contains a notice to be displayed to any user who relies on the certificate.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_POLICY_QUALIFIER_CPS(1.3.6.1.5.5.7.2.1)

</td>
<td>Identifies a pointer to a URI that contains the Certification Practice Statement (CPS) defined by the certification authority. </td>
</tr>
</table>
 



To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see the <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and the <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a> topics.

## -inheritance

The <b>IX509ExtensionCertificatePolicies</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionCertificatePolicies</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/win32/seccrypto/extensions">Extensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
