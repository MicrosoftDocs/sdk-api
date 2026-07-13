---
UID: NN:certenroll.IPolicyQualifier
title: IPolicyQualifier (certenroll.h)
description: Represents a qualifier that can be associated with a certificate policy.
helpviewer_keywords: ["IPolicyQualifier","IPolicyQualifier interface [Security]","IPolicyQualifier interface [Security]","described","certenroll/IPolicyQualifier","security.ipolicyqualifier"]
old-location: security\ipolicyqualifier.htm
tech.root: security
ms.assetid: 3804e372-17bb-458d-8da5-85d760fe5e60
ms.date: 12/05/2018
ms.keywords: IPolicyQualifier, IPolicyQualifier interface [Security], IPolicyQualifier interface [Security],described, certenroll/IPolicyQualifier, security.ipolicyqualifier
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
 - IPolicyQualifier
 - certenroll/IPolicyQualifier
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
 - IPolicyQualifier
---

# IPolicyQualifier interface


## -description

The <b>IPolicyQualifier</b> interface represents a qualifier that can be associated with a certificate policy. The following syntax shows the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structures that define <a href="/windows/desktop/SecGloss/c-gly">certificate policies</a> and their associated qualifiers. The value is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and included in the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> with the policy object it qualifies.

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
-- UserNotice
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


```
 Policy qualifiers can be used when an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) is considered insufficient to fully identify a policy. Qualifiers are defined by using the <b>IPolicyQualifier</b> interface and can be associated with a policy by adding qualifiers to the <a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifiers">IPolicyQualifiers</a> collection retrieved from an  <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a> object. A Windows <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> supports the following qualifiers.<table>
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
 



Unless one user notice in the chain duplicates another, all notices in the certificate path should be displayed to the relying party. To minimize duplication, this qualifier should be present only in the end entity certificate and certification authority certificates issued to other organizations. The user notice has two optional fields, <b>noticeRef</b> and  <b>explicitText</b>, that are not supported. Policies and policy qualifiers are used in <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a> objects.

## -inheritance

The <b>IPolicyQualifier</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IPolicyQualifier</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a>
