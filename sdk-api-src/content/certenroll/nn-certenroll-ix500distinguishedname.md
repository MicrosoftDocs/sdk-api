---
UID: NN:certenroll.IX500DistinguishedName
title: IX500DistinguishedName (certenroll.h)
description: Represents an X.500 distinguished name (DN).
helpviewer_keywords: ["IX500DistinguishedName","IX500DistinguishedName interface [Security]","IX500DistinguishedName interface [Security]","described","certenroll/IX500DistinguishedName","security.ix500distinguishedname"]
old-location: security\ix500distinguishedname.htm
tech.root: security
ms.assetid: 49f176d9-33f6-4bc1-992c-c613279b0969
ms.date: 12/05/2018
ms.keywords: IX500DistinguishedName, IX500DistinguishedName interface [Security], IX500DistinguishedName interface [Security],described, certenroll/IX500DistinguishedName, security.ix500distinguishedname
f1_keywords:
- certenroll/IX500DistinguishedName
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
- IX500DistinguishedName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX500DistinguishedName interface


## -description


The <b>IX500DistinguishedName</b> interface represents an X.500 distinguished name (DN). The X.500 series of networking standards covers electronic directory services. A distinguished name uniquely identifies (distinguishes) each entry in the directory from all other entries. Each DN consists of one or more relative distinguished names (RDNs).

The <b>subject</b> field of a PKCS #10 certificate request contains the DN of the entity requesting the certificate
<pre class="syntax" xml:space="preserve"><code>
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
</code></pre>The DN consists of a sequence of RDNs. Each RDN consists of a set of attributes, and each attribute consists of an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a value. The data type of the value is identified by the <b>DirectoryString</b> structure.
<pre class="syntax" xml:space="preserve"><code>
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
</code></pre> The following RDN keys and associated OIDs are currently supported.<table>
<tr>
<th>Key</th>
<th>OID</th>
<th>Description</th>
<th>RDN type</th>
</tr>
<tr>
<td>C</td>
<td>XCN_OID_COUNTRY_NAME</td>
<td>Contains a two-letter ISO 3166 country or region code.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>CN</td>
<td>XCN_OID_COMMON_NAME</td>
<td>Contains a common name.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>EEMAIL

</td>
<td>XCN_OID_RSA_emailAddr</td>
<td>Contains an email address.</td>
<td><b>IA5String</b></td>
</tr>
<tr>
<td>DC</td>
<td>XCN_OID_DOMAIN_COMPONENT</td>
<td>Contains one component of a Domain Name System (DNS) name.</td>
<td><b>IA5String</b></td>
</tr>
<tr>
<td>GGivenName

</td>
<td>XCN_OID_GIVEN_NAME</td>
<td>Contains the part of a person's name that is not a surname.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>I</td>
<td>XCN_OID_INITIALS</td>
<td>Contains a person's initials.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>L</td>
<td>XCN_OID_LOCALITY_NAME</td>
<td>Contains the locality name that identifies a city, country, or other geographic region.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>O</td>
<td>XCN_OID_ORGANIZATION_NAME</td>
<td>Contains the name of an organization.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>OU</td>
<td>XCN_OID_ORGANIZATIONAL_UNIT_NAME</td>
<td>Contains the name of a unit subdivision within an organization.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>SST

</td>
<td>XCN_OID_STATE_OR_PROVINCE_NAME</td>
<td>Contains the full name of a state or province.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>STREET</td>
<td>XCN_OID_STREET_ADDRESS</td>
<td>Contains the physical address.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>SN</td>
<td>XCN_OID_SUR_NAME</td>
<td>Contains the family name of a person.</td>
<td><b>PrintableString</b></td>
</tr>
<tr>
<td>TTITLE

</td>
<td>XCN_OID_TITLE</td>
<td>Contains the title of a person in the organization.</td>
<td><b>PrintableString</b></td>
</tr>
</table>
 



Each service that is  based on X.500 defines its own distinguished name string representation. For example, LDAP uses a comma-delimited list arranged from right to left. Active Directory uses a forward slash (/) and arranges the list from left to right. Other services use semicolons as separators. The following example shows an Active Directory entry for an employee named John Peoples who works in the pharmaceutical division of a company named Contoso, Ltd.
<pre class="syntax" xml:space="preserve"><code>
/c=gb/o=Contoso Ltd./ou=Contoso Pharmaceuticals/cn=John Peoples
</code></pre>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX500DistinguishedName</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX500DistinguishedName</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX500DistinguishedName</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-decode">Decode</a>
</td>
<td align="left" width="63%">
Initializes the object from a Unicode-encoded distinguished name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-encode">Encode</a>
</td>
<td align="left" width="63%">
Initializes the object from a string that contains a distinguished name.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX500DistinguishedName</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-get_encodedname">EncodedName</a>


</td>
<td align="left" width="63%">
Retrieves a Unicode-encoded distinguished name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix500distinguishedname-get_name">Name</a>


</td>
<td align="left" width="63%">
Retrieves a distinguished name.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/subject-names">Subject Names</a>
 

 

