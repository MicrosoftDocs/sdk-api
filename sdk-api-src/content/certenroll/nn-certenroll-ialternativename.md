---
UID: NN:certenroll.IAlternativeName
title: IAlternativeName
author: windows-sdk-content
description: Is used by an IX509ExtensionAlternativeNames object to represent an instance of an AlternativeNames extension.
old-location: security\ialternativename.htm
old-project: SecCertEnroll
ms.assetid: 2a6cfda8-b3cb-4a0f-bb65-b182c16207be
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IAlternativeName, IAlternativeName interface [Security], IAlternativeName interface [Security],described, certenroll/IAlternativeName, security.ialternativename
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IAlternativeName interface


## -description


A collection of  <b>IAlternativeName</b> interfaces is used by an <a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a> object to represent an instance of an <b>AlternativeNames</b> extension. The collection is represented by the <a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a> interface. The following syntax shows the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension.
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
</code></pre> You can initialize an <b>IAlternativeName</b> object from an <a href="https://msdn.microsoft.com/79b675cc-c979-46ab-aee1-0031af2efd40">AlternativeNameType</a> enumeration. The following types are available, but they are supported by different initialization methods as indicated.<table>
<tr>
<th>Value</th>
<th>Description</th>
<th>Initialization method</th>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_OTHER_NAME</td>
<td>The name consists of an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and a byte array.</td>
<td>
<a href="https://msdn.microsoft.com/cd697085-0e8e-4a18-a7c5-77cd4927f664">InitializeFromOtherName</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_RFC822_NAME</td>
<td>The name is an email address.</td>
<td>
<a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DNS_NAME</td>
<td>The name is a Domain Name System (DNS) name.</td>
<td>
<a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_DIRECTORY_NAME</td>
<td>The name is an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> directory name.</td>
<td>
<a href="https://msdn.microsoft.com/1559801c-ec62-471e-851f-f67219565cd1">InitializeFromRawData</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_URL</td>
<td>The name is a URL.</td>
<td>
<a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_IP_ADDRESS</td>
<td>The name is an Internet Protocol (IP) address.</td>
<td>
<a href="https://msdn.microsoft.com/1559801c-ec62-471e-851f-f67219565cd1">InitializeFromRawData</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_REGISTERED_ID</td>
<td>The name is a registered OID.</td>
<td>
<a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_GUID</td>
<td>The name is a GUID.</td>
<td>
<a href="https://msdn.microsoft.com/1559801c-ec62-471e-851f-f67219565cd1">InitializeFromRawData</a>
</td>
</tr>
<tr>
<td>XCN_CERT_ALT_NAME_USER_PRINCIPLE_NAME</td>
<td>The name is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN).</td>
<td>
<a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a>
</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAlternativeName</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAlternativeName</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/cd697085-0e8e-4a18-a7c5-77cd4927f664">InitializeFromOtherName</a>
</td>
<td align="left" width="63%">
Initializes the object from an OID and the associated raw data (byte array).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1559801c-ec62-471e-851f-f67219565cd1">InitializeFromRawData</a>
</td>
<td align="left" width="63%">
Initializes the object from a DSA GUID, an X.500 directory name, or an IP address contained in a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b5f7dd3-00dc-474b-8920-45a3acded209">InitializeFromString</a>
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

<a href="https://msdn.microsoft.com/be14756b-a7dc-40f4-ae09-b576f85837f6">ObjectId</a>


</td>
<td align="left" width="63%">
Retrieves the  OID, if any, associated with the name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7385654d-03f8-4796-a95c-000fa8ab65a3">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the DER-encoded byte array that contains the name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1d916450-4a4e-4f11-b95b-dbf9693b7cdd">StrValue</a>


</td>
<td align="left" width="63%">
Retrieves a string that contains an email address, a DNS name, a URL, a registered OID, or a UPN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="63%">
Retrieves the alternative name type.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://msdn.microsoft.com/facfcc85-c1ca-47a1-90a6-10522b15cc65">IX509ExtensionAlternativeNames</a>
 

 

