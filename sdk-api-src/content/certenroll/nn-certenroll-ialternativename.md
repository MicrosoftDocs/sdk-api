---
UID: NN:certenroll.IAlternativeName
title: IAlternativeName (certenroll.h)
author: windows-sdk-content
description: Is used by an IX509ExtensionAlternativeNames object to represent an instance of an AlternativeNames extension.
old-location: security\ialternativename.htm
tech.root: seccertenroll
ms.assetid: 2a6cfda8-b3cb-4a0f-bb65-b182c16207be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAlternativeName, IAlternativeName interface [Security], IAlternativeName interface [Security],described, certenroll/IAlternativeName, security.ialternativename
ms.topic: interface
f1_keywords: ["certenroll/IAlternativeName"]
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
 - IAlternativeName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAlternativeName interface


## -description


A collection of  <b>IAlternativeName</b> interfaces is used by an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a> object to represent an instance of an <b>AlternativeNames</b> extension. The collection is represented by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a> interface. The following syntax shows the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension.
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- AlternativeNames 
-- XCN_OID_SUBJECT_ALT_NAME2 (2.5.29.17)
----------------------------------------------------------------------

AltNames ::= SEQUENCE --#public-- OF GeneralName
GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
  otherName              [0] IMPLICIT OtherName,
  rfc822Name             [1] IMPLICIT IA5STRING,
  dNSName                [2] IMPLICIT IA5STRING,
  x400Address            [3] IMPLICIT SeqOfAny,       --Not supported
  directoryName          [4] EXPLICIT ANY,    
  ediPartyName           [5] IMPLICIT SeqOfAny,
  uniformResourceLocator [6] IMPLICIT IA5STRING,
  iPAddress              [7] IMPLICIT OCTETSTRING,
  registeredID           [8] IMPLICIT EncodedObjectID --Not supported
}

OtherName ::= SEQUENCE 
{
   type                    EncodedObjectID,
   value                   [0] EXPLICIT NOCOPYANY 
}
</code></pre> You can initialize an <b>IAlternativeName</b> object from an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-alternativenametype">AlternativeNameType</a> enumeration. The following types are available, but they are supported by different initialization methods as indicated.<table>
<tr>
<th>Value</th>
<th>Description</th>
<th>Initialization method</th>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_OTHER_NAME</td>
<td>The name consists of an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a byte array.</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromothername">InitializeFromOtherName</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_RFC822_NAME</td>
<td>The name is an email address.</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DNS_NAME</td>
<td>The name is a Domain Name System (DNS) name.</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DIRECTORY_NAME</td>
<td>The name is an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/x-gly">X.500</a> directory name.</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromrawdata">InitializeFromRawData</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_URL</td>
<td>The name is a URL.</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_IP_ADDRESS</td>
<td>The name is an Internet Protocol (IP) address.</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromrawdata">InitializeFromRawData</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_REGISTERED_ID</td>
<td>The name is a registered OID.</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_GUID</td>
<td>The name is a GUID.</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromrawdata">InitializeFromRawData</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</td>
<td>The name is a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN).</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a>
</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAlternativeName</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAlternativeName</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAlternativeName</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromothername">InitializeFromOtherName</a>
</td>
<td align="left" width="63%">
Initializes the object from an OID and the associated raw data (byte array).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromrawdata">InitializeFromRawData</a>
</td>
<td align="left" width="63%">
Initializes the object from a DSA GUID, an X.500 directory name, or an IP address contained in a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-initializefromstring">InitializeFromString</a>
</td>
<td align="left" width="63%">
Initializes the object from a string that contains an email address, a DNS name, a URL, a registered OID, or a UPN.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAlternativeName</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_objectid">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the  OID, if any, associated with the name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_rawdata">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the DER-encoded byte array that contains the name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_strvalue">StrValue</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains an email address, a DNS name, a URL, a registered OID, or a UPN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ialternativename-get_type">Type</a>


</td>
<td align="left" width="63%">
Retrieves the alternative name type.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ialternativenames">IAlternativeNames</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a>
 

 

