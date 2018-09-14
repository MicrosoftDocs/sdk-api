---
UID: NN:certenroll.IX509ExtensionCertificatePolicies
title: IX509ExtensionCertificatePolicies
author: windows-sdk-content
description: Enables you to specify a collection of policy information terms, each of which consists of an object identifier (OID) and optional policy qualifiers. A single policy term is defined by an ICertificatePolicy object.
old-location: security\ix509extensioncertificatepolicies.htm
tech.root: seccertenroll
ms.assetid: d35d155c-fb81-4d7e-b5c9-82ac5af4b79e
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509ExtensionCertificatePolicies, IX509ExtensionCertificatePolicies interface [Security], IX509ExtensionCertificatePolicies interface [Security],described, certenroll/IX509ExtensionCertificatePolicies, security.ix509extensioncertificatepolicies
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
 - IX509ExtensionCertificatePolicies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionCertificatePolicies interface


## -description


The <b>IX509ExtensionCertificatePolicies</b> interface enables you to specify a collection of policy information terms, each of which consists of an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and optional policy qualifiers. A single policy term is defined by an <a href="https://msdn.microsoft.com/2162de70-edcc-4f01-807d-79ff200d0016">ICertificatePolicy</a> object. The following syntax shows the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and included in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.
<pre class="syntax" xml:space="preserve"><code>
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
    
</code></pre>When included in a certificate issued to an end entity, this extension identifies the policies under which the certificate was issued and the purposes for which the certificate can be used. Applications that have specific policy requirements should compare these to the collection of policy <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) in the certificate.

When included in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> certificate, this extension limits the set of policies for the certification paths extending from the certification authority certificate. If a certification authority does not want to limit this set, it can assert <b>XCN_OID_ANY_CERT_POLICY</b> (2.5.29.32.0).

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
<td>Indicates that the certificate is issued with the highest security. For example, the issuance of a key recovery agent certificate can require additional background checks and a digital signature from a designated approver because a person holding this certificate can recover <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> material from the certification authority.</td>
</tr>
</table>
 



 Policy qualifiers can be used when an OID is considered insufficient to fully identify a policy. Qualifiers are defined by using the <a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a> interface and can be associated with a policy by adding qualifiers to the <a href="https://msdn.microsoft.com/da8b6289-379e-4dff-b15a-b0967f245c3d">IPolicyQualifiers</a> collection retrieved from an  <a href="https://msdn.microsoft.com/2162de70-edcc-4f01-807d-79ff200d0016">ICertificatePolicy</a> object. A Windows certification authority supports the following qualifiers.<table>
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
 



To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see the <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and the <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a> topics.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionCertificatePolicies</b> interface inherits from <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>. <b>IX509ExtensionCertificatePolicies</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionCertificatePolicies</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd542fbd-4cba-4584-9a14-b22cf0ae5705">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  object from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3134c668-afe6-447b-9f0e-8c21df36e131">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the object from an <a href="https://msdn.microsoft.com/2503adcb-0b73-42ef-98cf-a2b906e34ef7">ICertificatePolicies</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionCertificatePolicies</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/eefb515d-62dc-4ad7-b0c4-c65a4da5742e">Policies</a>


</td>
<td align="left" width="63%">
Retrieves a collection of certificate policies.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/f2a6854d-1831-489f-adf6-31a0b26511e3">Extensions</a>



<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

