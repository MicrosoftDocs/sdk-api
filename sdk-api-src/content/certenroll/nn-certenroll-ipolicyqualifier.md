---
UID: NN:certenroll.IPolicyQualifier
title: IPolicyQualifier
author: windows-sdk-content
description: Represents a qualifier that can be associated with a certificate policy.
old-location: security\ipolicyqualifier.htm
tech.root: SecCertEnroll
ms.assetid: 3804e372-17bb-458d-8da5-85d760fe5e60
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPolicyQualifier, IPolicyQualifier interface [Security], IPolicyQualifier interface [Security],described, certenroll/IPolicyQualifier, security.ipolicyqualifier
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
 - IPolicyQualifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPolicyQualifier interface


## -description


The <b>IPolicyQualifier</b> interface represents a qualifier that can be associated with a certificate policy. The following syntax shows the <a href="https://msdn.microsoft.com/en-us/library/ms721532(v=VS.85).aspx">Abstract Syntax Notation One</a> (ASN.1) structures that define <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate policies</a> and their associated qualifiers. The value is encoded by using <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) and included in the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a> with the policy object it qualifies.
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

</code></pre> Policy qualifiers can be used when an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) is considered insufficient to fully identify a policy. Qualifiers are defined by using the <b>IPolicyQualifier</b> interface and can be associated with a policy by adding qualifiers to the <a href="https://msdn.microsoft.com/en-us/library/Aa376804(v=VS.85).aspx">IPolicyQualifiers</a> collection retrieved from an  <a href="https://msdn.microsoft.com/en-us/library/Aa375225(v=VS.85).aspx">ICertificatePolicy</a> object. A Windows <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> supports the following qualifiers.<table>
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
 



Unless one user notice in the chain duplicates another, all notices in the certificate path should be displayed to the relying party. To minimize duplication, this qualifier should be present only in the end entity certificate and certification authority certificates issued to other organizations. The user notice has two optional fields, <b>noticeRef</b> and  <b>explicitText</b>, that are not supported. Policies and policy qualifiers are used in <a href="https://msdn.microsoft.com/en-us/library/Aa378121(v=VS.85).aspx">IX509ExtensionCertificatePolicies</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPolicyQualifier</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IPolicyQualifier</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IPolicyQualifier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa376813(v=VS.85).aspx">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the object from a string and a value that identifies the qualifier type.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPolicyQualifier</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376815(v=VS.85).aspx">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the OID for the qualifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376817(v=VS.85).aspx">Qualifier</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains the qualifier used to initialize the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376818(v=VS.85).aspx">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the DER-encoded qualifier object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa376819(v=VS.85).aspx">Type</a>


</td>
<td align="left" width="63%">
Retrieves the qualifier type.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376803(v=VS.85).aspx">IPolicyQualifier</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378121(v=VS.85).aspx">IX509ExtensionCertificatePolicies</a>
 

 

