---
UID: NN:certenroll.ICertificatePolicy
title: ICertificatePolicy (certenroll.h)
description: Can be used to specify a certificate policy that identifies a purpose for which the certificate can be used.helpviewer_keywords: ["ICertificatePolicy","ICertificatePolicy interface [Security]","ICertificatePolicy interface [Security]","described","certenroll/ICertificatePolicy","security.icertificatepolicy"]
old-location: security\icertificatepolicy.htm
tech.root: seccertenroll
ms.assetid: 2162de70-edcc-4f01-807d-79ff200d0016
ms.date: 12/05/2018
ms.keywords: ICertificatePolicy, ICertificatePolicy interface [Security], ICertificatePolicy interface [Security],described, certenroll/ICertificatePolicy, security.icertificatepolicy
f1_keywords:
- certenroll/ICertificatePolicy
dev_langs:
- c++
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
- ICertificatePolicy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertificatePolicy interface


## -description


The <b>ICertificatePolicy</b> interface can be used to specify a certificate policy that identifies a purpose for which the certificate can be used. The policies are collected into an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a> object that you can use to initialize an  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a> or <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionmsapplicationpolicies">IX509ExtensionMSApplicationPolicies</a> object.

 The following syntax shows the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  used by both extension objects. The extension values are encoded by using <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the certificate request. A certificate policies collection consists of a sequence of <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) and optional sequence of policy qualifiers for each policy OID.<div class="alert"><b>Note</b>  Policy qualifiers, defined by the  <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a> interface, are used by a <b>CertificatePolicies</b> extension but not by an <b>MSApplicationPolicies</b> extension.</div>
<div> </div>

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
</code></pre> Issuance policies, defined by an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a> object, identify the extent to which the identity presented in the certificate is trusted. The following policies are predefined. The <i>x.y.z</i> portion of each OID represents a randomly generated numeric sequence that is unique for each forest. You can also create custom OIDs to represent custom issuance policies.<table>
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
<td>Indicates that the certificate is issued with the highest security. For example, the issuance of a key recovery agent certificate can require additional background checks and a digital signature from a designated approver because a person holding this certificate can recover private key material from the CA.</td>
</tr>
</table>
 



Application policies, defined by an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionmsapplicationpolicies">IX509ExtensionMSApplicationPolicies</a> object, enable an application to filter certificates by comparing the policy OIDs it will accept to the policy OIDs contained in the certificate. The <b>MSApplicationPolicies</b> extension is very similar to the <b>EnhancedKeyUsage</b> extension but is often used for policy mapping.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificatePolicy</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertificatePolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertificatePolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertificatepolicy-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from an OID.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertificatePolicy</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertificatepolicy-get_objectid">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves an OID for the policy object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertificatepolicy-get_policyqualifiers">PolicyQualifiers</a>


</td>
<td align="left" width="63%">
Retrieves a collection of optional policy qualifiers that can be applied to a certificate policy.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a>
 

 

